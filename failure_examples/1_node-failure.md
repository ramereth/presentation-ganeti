!SLIDE center transition=fade

# Primary node failure #

![primary-failure](primary-failure.png)

!SLIDE center transition=fade

# Primary node failure #

![primary-failover](primary-failover.png)

    $ gnt-instance failover --ignore-consistency web

!SLIDE center transition=fade

# Secondary node failure #

![secondary-failover](secondary-failover.png)

    $ gnt-instance replace-disks --on-secondary \
        --new-secondary=node1 web
