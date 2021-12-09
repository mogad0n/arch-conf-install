# Audit Framework

## Kernel

To ensure that all process which may have started before `auditd` are marked as auditable use boot time kernel param `audit=1`.

## Userspace

* Install the `audit` package, enable and start the `auditd.service`.
* The config file is `auditd.conf`.
* The rules are defined in `/etc/audit/audit.rules`.
* `auditctl` can be used to edit rules on the fly.
* `ausearch` and `aureport` are used to summarize and view data.
