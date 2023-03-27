## Role description

This role can be used to take a snapshot of a (Linux / Windows) VM running on a VMware hypervisor.<br>
Snapshot will be saved next to the VM.

------

## Prerequisites

Access to the `TCP 443` port of your vCenter, and the **PyVmomi** module.

------

## Input variables

You need to declare the FQDN or IP address of your vCenter instance, your credentials and datacenter location.

```yaml
vcenter_hostname: 192.168.3.245
vsphere_username: administrator@home.lab
vsphere_password: ********
datacenter_name: DC1.lab
```

Sensitive credentials should be stored in an Ansible vault.

An optional snapshot comment can be set :

```yaml
snapshot_comment: "Before OS update"
```

Otherwiwe, a default comment will be used.

------

## Targets compatibility

This role has been tested on the following VMware versions :
- [x] vCenter 7.0 U3e

------

## Usage

```bash
$ ansible-playbook playbooks/vmware_snapshot.yml -i inventories/foo -l bar
```

------

## History

| 2022/06/21 | 1.0.0 | initial release                                           |
| ---------- | ----- | --------------------------------------------------------- |
