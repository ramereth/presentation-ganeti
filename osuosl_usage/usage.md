!SLIDE smbullets transition=fade

# Ganeti usage at OSUOSL #

* 4-node production OSUOSL cluster
* Project clusters (OSGeo, ORVSD, OSDV, phpBB, etc)
* ~64 virtual instances
* qemu-kvm 0.11.x
* 64bit Gentoo Linux

## Node details ##

* DL360 G4
* 24G RAM
* 630G - RAID5 6x146G 10K SCSI HDDs

!SLIDE center transition=fade

## Xen + iSCSI vs. kvm + DRBD ##

![busybox](busybox.png)

!SLIDE center small-img-height transition=fade

# Ganeti node CPU usage #

![g2-cpu](g2-cpu.png)

!SLIDE center transition=fade

# Ganeti node LOAD #

![g2-load](g2-load.png)

!SLIDE center transition=fade

# Ganeti node DRBD network #

![g2-eth1](g2-eth1.png)

!SLIDE bullets transition=fade

# OSUOSL future ganeti plans #

* KSM (Kernel SamePage Merging)
* Upgrade to qemu-kvm 0.12.x
* Migrate hosts from libvirt
* Puppet integration
* Web-based tools
* libcloud
