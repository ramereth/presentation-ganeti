!SLIDE bullets transition=fade

# Ganeti htools #

* Automatic allocation tools
* Cluster rebalancer - <code>hbal(1)</code>
* IAllocator plugin - <code>hail(1)</code>
* Cluster capacity estimator - <code>hspace(1)</code>

!SLIDE commandline transition=fade

# <code>hbal</code> #

    $ hbal -m ganeti.osuosl.bak
    Loaded 4 nodes, 63 instances
    Initial check done: 0 bad nodes, 0 bad instances.
    Initial score: 0.53388595
    Trying to minimize the CV...
        1. bonsai            g1:g2 => g2:g1 0.53220090 a=f
        2. connectopensource g3:g1 => g1:g3 0.53114943 a=f
        3. amahi             g2:g3 => g3:g2 0.53088116 a=f
        4. mertan            g1:g2 => g2:g1 0.53031862 a=f
        5. dspace            g3:g1 => g1:g3 0.52958328 a=f
    Cluster score improved from 0.53388595 to 0.52958328
    Solution length=5

!SLIDE commandline transition=fade

# <code>hspace</code> #

    $ hspace --memory 512 --disk 10240 -m ganeti.osuosl.bak
    HTS_INI_INST_CNT=63

    HTS_FIN_INST_CNT=101

    HTS_ALLOC_INSTANCES=38
    HTS_ALLOC_FAIL_REASON=FAILDISK

!SLIDE commandline small transition=fade

# <code>hail</code> #

    $ gnt-instance add -t drbd -I hail \
    $   -s 10G -o image+gentoo-hardened-cf \
    $   --net 0:link=br42  web.example.org \
     - INFO: Selected nodes for instance web.example.org 
             via iallocator hail: gtest1.osuosl.bak, gtest2.osuosl.bak
    * creating instance disks...
    adding instance web.example.org to cluster config
     - INFO: Waiting for instance web.example.org to sync disks.
     - INFO: - device disk/0:  3.60% done, 1149 estimated seconds remaining
     - INFO: - device disk/0: 29.70% done, 144 estimated seconds remaining
     - INFO: - device disk/0: 55.50% done, 88 estimated seconds remaining
     - INFO: - device disk/0: 81.10% done, 47 estimated seconds remaining
     - INFO: Instance web.example.org's disks are in sync.
    * running the instance OS create scripts...
    * starting instance...

