!SLIDE bullets transition=fade

# Ganeti administration #

* Administration via single master node
* All commands support interactive help
* Consistent command line interface
*  __`gnt-<command>`__

!SLIDE bullets transition=fade

# Ganeti Commands #

* `gnt-cluster`
* `gnt-node`
* `gnt-instance`
* `gnt-backup`
* `gnt-os`

!SLIDE bullets transition=fade

# `gnt-cluster` #

* Cluster-wide configuration
* Initialize & destroy cluster
* Fail-over master node
* Verify cluster integrity

!SLIDE bullets transition=fade

# `gnt-node` #

* Node-wide configuration/administration
* Add & remove cluster nodes
* Relocate all secondary instances from a node
* List information about nodes

!SLIDE bullets transition=fade

# `gnt-instance` #

* Per-instance configuration/administration
* Add, remove, rename, & reinstall instance
* Serial console
* Fail-over instance, change secondary
* Stop, start, migrate instance
* List instance information

!SLIDE bullets transition=fade

# `gnt-backup` #

* Export instance to an image
* Import instance from an exported image
* Useful for inter-cluster migration
