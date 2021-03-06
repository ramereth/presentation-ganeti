!SLIDE bullets transition=fade

# What is ganeti? #

* Software to manage a cluster of virtual servers
* Project created & maintained by Google
* Combines virtualization & data replication
* Supports multiple hypervisors
* Automates VM storage management
* Streamlines VM deployment

!SLIDES bullets smaller-img-height img-right transition=fade

# Ganeti software requirements #

![requirements](requirements.png)

* Python
* various python modules 
* DRBD
* LVM
* KVM, Xen, or LXC*

!SLIDE smbullets smaller-img-height center transition=fade

# Ganeti terminology #

* Cluster - group of nodes
* Node - physical host
* Instance - virtual machine, aka guest

![ganeti-cluster](ganeti-cluster.png )
