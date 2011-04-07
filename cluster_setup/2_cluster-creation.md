!SLIDE commandline smaller-img center transition=fade

# Cluster creation #

![cluster-creation](cluster-creation.png)

    $ gnt-cluster init \
          --master-netdev=br42 \
          --vg-name ganeti \
          -s 10.1.11.200 \
          --enabled-hypervisors=kvm \
          -N link=br113 \
          -B vcpus=2,memory=512M \
          -H kvm:kernel_path=/boot/guest/vmlinuz-x86_64 \
          ganeti-cluster.osuosl.org

!SLIDE commandline center transition=fade incremental

# Adding nodes #

![adding-nodes](adding-nodes.png)

    $ gnt-node add -s 10.1.11.201 node2

!SLIDE commandline center transition=fade incremental

# Listing nodes

![adding-nodes](adding-nodes.png)

    $ gnt-node list
    Node          DTotal  DFree MTotal MNode MFree Pinst Sinst
    g1.osuosl.bak 673.9G 163.8G  23.6G 16.8G  8.3G    18    18
    g2.osuosl.bak 673.9G 149.2G  23.6G 16.1G 10.5G    18    17
    g3.osuosl.bak 673.9G 120.5G  23.6G 16.3G  9.5G    18    18
    g4.osuosl.bak 673.9G 100.0G  23.6G 16.4G  9.3G    17    18

!SLIDE commandline transition=fade incremental

# Cluster verification #

![adding-nodes](adding-nodes.png)

    $ gnt-cluster verify
    Sun Feb 20 2011 * Verifying global settings
    Sun Feb 20 2011 * Gathering data (4 nodes)
    Sun Feb 20 2011 * Gathering disk information (4 nodes)
    Sun Feb 20 2011 * Verifying node status
    Sun Feb 20 2011 * Verifying instance status
    Sun Feb 20 2011 * Verifying orphan volumes
    Sun Feb 20 2011 * Verifying orphan instances
    Sun Feb 20 2011 * Verifying N+1 Memory redundancy
    Sun Feb 20 2011 * Other Notes
    Sun Feb 20 2011 * Hooks Results

!SLIDE commandline small transition=fade

# Cluster information #

    $ gnt-cluster info
    Modification time: 2011-02-16 21:22:04
    Master node: g1.osuosl.bak
    Architecture (this node): 64bit (x86_64)
    Tags: (none)
    Default hypervisor: kvm
    Enabled hypervisors: kvm
    Hypervisor parameters:
      - kvm:
          boot_order: disk
          disk_type: paravirtual
          initrd_path: 
          kernel_args: ro
          kernel_path: /boot/guest/vmlinuz-x86_64-hardened
          nic_type: paravirtual
          root_path: /dev/vda2
          serial_console: True
          vnc_bind_address: 0.0.0.0
    OS-specific hypervisor parameters:
    OS parameters:
    Cluster parameters:
      - candidate pool size: 4
      - master netdev: br42
      - lvm volume group: ganeti
      - lvm reserved volumes: (none)
      - drbd usermode helper: /bin/true
      - file storage path: /var/lib/ganeti/export
      - maintenance of node health: False
      - uid pool: 
      - default instance allocator: hail
      - primary ip version: 4
    ...
