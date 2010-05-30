!SLIDE commandline center incremental small transition=fade

# Creating an instance #

![creating-instance](creating-instance.png)

    $ gnt-instance add -t drbd -n gtest1:gtest2 \
    $    -s 10G -o image+gentoo-hardened-cf \
    $    --net 0:link=br42  web.example.org
    * creating instance disks...
    adding instance web.example.org to cluster config
     - INFO: Waiting for instance web.example.org to sync disks.
     - INFO: - device disk/0:  3.90% done, 205 estimated seconds remaining
     - INFO: - device disk/0: 29.40% done, 101 estimated seconds remaining
     - INFO: - device disk/0: 54.90% done, 102 estimated seconds remaining
     - INFO: - device disk/0: 80.40% done, 41 estimated seconds remaining
     - INFO: - device disk/0: 98.40% done, 3 estimated seconds remaining
     - INFO: - device disk/0: 100.00% done, 0 estimated seconds remaining
     - INFO: - device disk/0: 100.00% done, 0 estimated seconds remaining
     - INFO: Instance web.example.org's disks are in sync.
    * running the instance OS create scripts...
    * starting instance...

!SLIDE commandline transition=fade

# Other instance commands #

    $ gnt-instance console web

    $ gnt-instance migrate web

    $ gnt-instance failover web

    $ gnt-instance reinstall -o image+ubuntu-lucid web

    $ gnt-instance info web

    $ gnt-instance list
