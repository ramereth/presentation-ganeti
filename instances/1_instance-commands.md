!SLIDE commandline center incremental small transition=fade

# Creating an instance #

![creating-instance](creating-instance.png)

    $ gnt-instance add -t drbd -n node3:node2 \
    $    -s 10G -o image+ubuntu-maverick \
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
     - INFO: Instance web.example.org's disks are in sync.
    * running the instance OS create scripts...
    * starting instance...

!SLIDE commandline small transition=fade

# List all instances #

    $ gnt-instance list
    Instance    OS                       Primary_node   Status    Memory
    ads         image+debian-lenny       phobos         running   1.0G
    area51      image+debian-lenny       deimos         running   3.0G
    code        image+debian-lenny       deimos         running   4.0G
    db1         image+gentoo-hardened-cf phobos         running   4.0G
    db2         image+gentoo-hardened-cf deimos         running   4.0G
    demo        image+debian-lenny       deimos         running   512M
    lists       image+gentoo-hardened-cf phobos         running   2.0G
    mail        image+debian-lenny       deimos         running   1.0G
    misc        image+debian-lenny       deimos         running   2.0G
    testing     image+debian-lenny       phobos         running   2.0G
    www         image+gentoo-hardened-cf phobos         running   2.0G

!SLIDE commandline transition=fade

# Other instance commands #

    $ gnt-instance console web

    $ gnt-instance migrate web

    $ gnt-instance failover web

    $ gnt-instance reinstall -o image+ubuntu-lucid web

    $ gnt-instance info web

    $ gnt-instance list
