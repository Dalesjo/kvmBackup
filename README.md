# kvmBackup
Simple script to backup your kvm configuration and your lvm partition. Both files are encrypted and stored in a tar archive with readme on howto restore. To run, use the command below

```bash
kvmBackup -k mq -l /dev/virtualMachines/mq -d /backup -p yourpassword
```

* mq is the name off the virtual machine
* /dev/virtualMachines/mq is the path to the lvm partition that need to be copied.
* yourpassword is the string used to encrypt your partition and configuration during backup.

### Important
* Only works with virsh
* Virtual Machine must store its data on lvm partition.
* Virtual Machine is powered off before snapshot is done.
