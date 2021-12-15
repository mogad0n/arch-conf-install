# Power Management Tools

## Tools and their configurations

### cpupower

* `cpupower` and the AUR `cpupower-gui` are the relevant packages.
* These are a set of userspace utilities designed to assist with CPU frequency scaling.
* the configuration is located at `/etc/default/cpupower`
* __Enable__ and _start_ the systemd service.

### Power Profile Daemons

* look into [PPD](https://wiki.archlinux.org/title/CPU_frequency_scaling#power-profiles-daemon)
* using 'performance'.

## thermald

* The `thermald` package is a Linux daemon used to prevent the overheating of Intel CPUs. This daemon monitors temperature and applies compensation  using available cooling methods.
* _Start_ and __enable__ the systemd service
