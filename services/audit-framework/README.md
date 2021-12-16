# Audit Framework

## Kernel

To ensure that all process which may have started before `auditd` are marked as auditable use boot time kernel param `audit=1`.

## Userspace

* Install the `audit` package, enable and start the `auditd.service`.
* The config file is `auditd.conf`.
* The rules are defined in `/etc/audit/audit.rules`.
* `auditctl` can be used to edit rules on the fly.
* `ausearch` and `aureport` are used to summarize and view data.


## Rules

* Read from `/etc/audit/auditd.rules`

* If for example `/etc/audit/rules.d/syscalls.rules` is the sort of structure being followed,
  `augenrules` is used to merge all the component rules files.
    * It is recommended to run first with the `--check` flag and `--load` can be used if there were no errors found.
    * The files are concatenated in order, based on their natural sort (see -v option of ls(1)) and stripped of empty and comment (#) lines.

* rulesets:
    * syscalls
        * format: `-a action,list -S syscall -F field=value -k keyname`
    * files
        * format: `-w path-to-file -p permissions -k keyname`
    * ..?



## Further Reading

* `man` pages (list here)
* archwiki article
* syscalls docs
* update the format for rules
