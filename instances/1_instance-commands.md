!SLIDE center transition=scrollLeft

# Creating an instance #

![creating-instance](creating-instance.png)

!SLIDE commandline incremental small transition=scrollLeft

# Creating an instance #

    $ gnt-instance add -t drbd -n gtest1:gtest2 \
    $    -s 10G -o image+gentoo-hardened-cf \
    $    --net 0:link=br42  gimager.osuosl.bak
    * creating instance disks...
    adding instance gimager.osuosl.bak to cluster config
     - INFO: Waiting for instance gimager.osuosl.bak to sync disks.
     - INFO: - device disk/0:  3.90% done, 205 estimated seconds remaining
     - INFO: - device disk/0: 29.40% done, 101 estimated seconds remaining
     - INFO: - device disk/0: 54.90% done, 102 estimated seconds remaining
     - INFO: - device disk/0: 80.40% done, 41 estimated seconds remaining
     - INFO: - device disk/0: 98.40% done, 3 estimated seconds remaining
     - INFO: - device disk/0: 100.00% done, 0 estimated seconds remaining
     - INFO: - device disk/0: 100.00% done, 0 estimated seconds remaining
     - INFO: Instance gimager.osuosl.bak's disks are in sync.
    * running the instance OS create scripts...
    * starting instance...

!SLIDE commandline transition=scrollLeft

# Other instance commands #

    $ gnt-instance console gimager
    $ gnt-instance migrate gimager
    $ gnt-instance failover gimager
    $ gnt-instance reinstall -o image+ubuntu-lucid gimager
    $ gnt-instance info gimager
    $ gnt-instance list
