!SLIDE center transition=scrollLeft

# Primary node failure #

![primary-failure](primary-failure.png)


!SLIDE center transition=scrollLeft

# Primary node failure #

    $ gnt-instance failover --ignore-consistency gimager

![primary-failover](primary-failover.png)


!SLIDE center transition=scrollLeft

# Secondary node failure #

    $ gnt-instance replace-disks --on-secondary \
    $   --new-secondary=node1 gimager

![secondary-failover](secondary-failover.png)
