!SLIDE bullets transition=fade

# Ganeti administration #

* Administration via single master node
* All commands support interactive help
* Consistent commandline interface
*  __`gnt-<command>`__

!SLIDE bullets transition=fade

# Ganeti Commands #

* `gnt-cluster`
* `gnt-node`
* `gnt-instance`
* `gnt-backup`
* `gnt-os`

!SLIDE bullets transition=fade incremental

# `gnt-cluster` #

* Cluster commands
* Initialize, destroy cluster
* Fail-over master node
* Verify cluster integrity

!SLIDE bullets transition=fade incremental

# `gnt-node` #

* Add & remove cluster nodes
* Fail-over/migrate all primary instances on a node
* Relocate all secondary instances from a node
* List information about nodes

!SLIDE bullets transition=fade incremental 

# `gnt-instance` #

* Add, remove, rename, & reinstall instance
* Connect to serial console
* Fail-over instance, change secondary
* Stop, start, migrate instance
* List instance information

!SLIDE bullets transition=fade incremental 

# `gnt-backup` #

* Export instance to an image
* Import instance from an exported image
* Useful for inter-cluster migration
