!SLIDE commandline center transition=fade incremental

# Cluster creation #

<span class="smimage">
![cluster-creation](cluster-creation.png)
</span>

    $ gnt-cluster init \
          --master-netdev=br42 \
          -g ganeti -s 10.1.11.200 \
          --enabled-hypervisors=kvm \
          -N link=br113 \
          -B vcpus=2,memory=512M \
          -H kvm:kernel_path=/boot/guest/vmlinuz-x86_64 \
          ganeti-cluster.osuosl.org

!SLIDE commandline center transition=fade incremental

# Adding nodes #

![adding-nodes](adding-nodes.png)

    $ gnt-node add \
        -s 10.1.11.201 node2

!SLIDE commandline transition=fade incremental

# Cluster verification #

    $ gnt-cluster verify
    Wed Jun  2 17:31:07 2010 * Verifying global settings
    Wed Jun  2 17:31:08 2010 * Gathering data (4 nodes)
    Wed Jun  2 17:31:09 2010 * Verifying node status
    Wed Jun  2 17:31:09 2010 * Verifying instance status
    Wed Jun  2 17:31:09 2010 * Verifying orphan volumes
    Wed Jun  2 17:31:09 2010 * Verifying oprhan instances
    Wed Jun  2 17:31:09 2010 * Verifying N+1 Memory redundancy
    Wed Jun  2 17:31:09 2010 * Other Notes
    Wed Jun  2 17:31:09 2010 * Hooks Results

!SLIDE commandline small transition=fade

## Cluster information ##

    $ gnt-cluster info
    Cluster name: ganeti-test.osuosl.bak
    Cluster UUID: a22576ba-9158-4336-8590-a497306f84b9
    Creation time: 2010-04-08 00:08:29
    Modification time: 2010-05-07 22:33:34
    Master node: gtest1.osuosl.bak
    Architecture (this node): 64bit (x86_64)
    Tags: (none)
    Default hypervisor: kvm
    Enabled hypervisors: kvm
    Hypervisor parameters:
      - kvm:
          acpi: True
          boot_order: disk
          cdrom_image_path: 
          disk_cache: default
          disk_type: paravirtual
          initrd_path: 
          kernel_args: ro
          kernel_path: /boot/guest/vmlinuz-x86_64-hardened
          kvm_flag: 
          migration_port: 8102
          nic_type: paravirtual
          root_path: /dev/vda2
          security_domain: 
          security_model: none
          serial_console: True
          usb_mouse: 
          use_localtime: False
          vnc_bind_address: 0.0.0.0
          vnc_password_file: 
          vnc_tls: False
          vnc_x509_path: 
          vnc_x509_verify: False

!SLIDE command small transition=fade

## Cluster information ##

    OS specific hypervisor parameters:
    Cluster parameters:
      - candidate pool size: 10
      - master netdev: br42
      - lvm volume group: ganeti
      - file storage path: /var/lib/ganeti-storage/file
      - maintenance of node health: False
      - uid pool: 
    Default instance parameters:
      - default:
          auto_balance: True
          memory: 512
          vcpus: 2
    Default nic parameters:
      - default:
          link: br113
          mode: bridged
