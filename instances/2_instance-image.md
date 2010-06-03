!SLIDE smbullets transition=fade

# OS Installation #

* Bash scripts
* Format, mkfs, mount, install OS
* Hooks

## OS Definitions ##
* debootstrap
* FAI
* Disk image

!SLIDE bullets transition=fade

# `ganeti-instance-image` #
### http://code.osuosl.org/projects/ganeti-image ###

* Disk image based (filesystem dump or tarball)
* Flexible OS support
* Fast instance deployment ( ~30 seconds)

!SLIDE bullets transition=fade

# `ganeti-instance-image` #

* Setup serial for grub, grub2, & login prompt
* Automatic networking setup (DHCP or static)
* Automatic ssh hostkey regen
* Add optional kernel parameters to grub
