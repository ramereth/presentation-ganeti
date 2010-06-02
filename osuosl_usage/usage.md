!SLIDE smbullets transition=fade

# Ganeti usage at OSUOSL #

* 4-node production cluster
* Several project clusters (OSGeo, ORVSD, OSDV, phpBB, etc)
* ~64 virtual instances
* qemu-kvm 0.11
* 64bit Gentoo Linux

## Node details ##

* DL360 G4
* 24G RAM
* 630G - RAID5 6x146G 10K SCSI HDDs

!SLIDE center transition=fade

# iSCSI vs. DRBD #

![busybox](busybox.png)

!SLIDE center transition=fade

# Ganeti node CPU #

<span class="height-image">
![g2-cpu](g2-cpu.png)
</span>

!SLIDE center transition=fade

# Ganeti node LOAD #

![g2-load](g2-load.png)

!SLIDE center transition=fade

# Ganeti node DRBD #

![g2-eth1](g2-eth1.png)

!SLIDE bullets transition=fade

# OSUOSL future ganeti plans #

* KSM (Kernel SamePage Merging)
* Upgrade to qemu-kvm 0.12
* Migrate hosts from libvirt
* Puppet integration
* Web-based tools
* libcloud
