!SLIDE bullets transition=fade

# Ganeti htools #

* Automatic allocation tools
* Cluster rebalancer - __`hbal`__
* IAllocator plugin - __`hail`__
* Cluster capacity estimator - __`hspace`__

!SLIDE commandline transition=fade

# __`hbal`__ #

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

# __`hbal`__ #

    $ hbal -C -m ganeti.osuosl.bak
    Loaded 4 nodes, 71 instances
    Initial check done: 0 bad nodes, 0 bad instances.
    Initial score: 2.10591985
    Trying to minimize the CV...
        1. linuxfund            g4:g3 => g4:g2 2.09981699 a=r:g2
    Cluster score improved from 2.10591985 to 2.09981699
    Solution length=1

    Commands to run to reach the above solution:
      
      echo jobset 1, 1 jobs
        echo job 1/1
        gnt-instance replace-disks -n g2 linuxfund

!SLIDE commandline transition=fade

# __`hspace`__ #

    $ hspace --memory 512 --disk 10240 -m ganeti.osuosl.bak
    HTS_INI_INST_CNT=63

    HTS_FIN_INST_CNT=101

    HTS_ALLOC_INSTANCES=38
    HTS_ALLOC_FAIL_REASON=FAILDISK

!SLIDE commandline small transition=fade

# __`hail`__ #

    $ gnt-instance add -t drbd -I hail \
    $   -s 10G -o image+ubuntu-maverick \
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
