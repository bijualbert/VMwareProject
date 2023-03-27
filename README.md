Collection of Ansible roles to be used with a VMware hypervisor :
- [vm_create] : creates a VM from a template
- [vm_snapshot] : takes a snapshot of a VM
- [vm_add_disks] : adds disk(s) to an existing VM
- [vm_snapshots_remove] : removes all snapshots of a VM.

------

They require :
- a vCenter instance
- access to the `TCP 443` port of your vCenter
- proper credentials.
