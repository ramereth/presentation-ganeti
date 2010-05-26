!SLIDE full-page-image transition=scrollLeft

# Primary node failure #

### image ###

!SLIDE commandline transition=scrollLeft

# Primary node failure #

    $ gnt-instance failover --ignore-consistency gimager

### image ###

!SLIDE commandline transition=scrollLeft

# Secondary node failure #

    $ gnt-instance replace-disks --on-secondary \
    $   --new-secondary=node1 gimager

### image ###
