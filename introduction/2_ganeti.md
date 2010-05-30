!SLIDE bullets transition=fade

# What I will cover #

* Ganeti terminology, comparisons, & goals
* Cluster & virtual machine setup
* Failure walk through
* OSUOSL usage of ganeti
* Future roadmap

!SLIDE bullets transition=fade

# What is ganeti? #

* Software to manage clusters of virtual servers
* Combines virtualization & data replication
* Disk creation management
* Automated OS deployment

!SLIDE smbullets transition=fade

# Ganeti terminology #

## Node ##
* Physical machine
* Xen Dom0

## Instance ##
* Virtual machine
* Xen DomU
* Guest

!SLIDES smbullets transition=fade

# Ganeti technology #

## DRBD ##
* Distributed Replication Block Device (http://www.drbd.org)
* Used for data replication

## LVM (Logical Volume Manager) ##
* Used to manage instances' volumes

## Hypervisor ##
* KVM
* Xen
