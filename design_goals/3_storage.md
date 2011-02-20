!SLIDE bullets transition=fade

# Storage Options #
* LVM
* LVM + DRBD (supports migration)
* File based (raw, qcow2, etc)
* Shared storage patch coming soon!

!SLIDE smbullets center transition=fade

# Storage: LVM + DRBD #

![drbd](drbd.png)

* Primary & secondary storage nodes
* Each instance disk synced separately
* Dedicated backend DRBD network
* Allows instance failover & migration
* Ganeti manages setup, starting/stopping DRBD devices
