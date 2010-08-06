!SLIDE smbullets transition=fade

# Guest OS Installation #

* Bash scripts
* Format, mkfs, mount, install OS
* Hooks

## OS Definitions ##
* debootstrap
* Disk image
* Other OS-specific

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
