## Role description

This role can be used to create a Linux VM running on top of a VMware hypervisor.

------

## Prerequisites

Access to the TCP 443 port of your vCenter, and the **PyVmomi** module.

------

## Input variables

You need to declare the FQDN or IP address of your Prism Element / Prism Central, and your credentials.

```yaml
vcenter_hostname: vcenter.home.lab
vsphere_username: administrator@home.lab
vsphere_password: mysuperpassw0rd
```

Sensitive credentials should be stored in an Ansible vault.

Default root password (built in your VM templates) need to be specified :

```yaml
template_password: myrootpassw0rd
```

To set your VM's specs :

```yaml
vm_template: T-oraclelinux-85-k8s
vm_datastore: SSD
vm_folder: Temporary
vm_cpu: 2
vm_ram: 4
```

To set your VM's network settings (one NIC only) :

```yaml
vm_network: "VM Network"
vm_ip: 192.168.3.111
vm_gateway: 192.168.3.254
vm_netmask: 255.255.255.0
```

------

## Targets compatibility

This role has been tested on the following Nutanix versions :
- [x] vCenter 7.0 U3d

------

## Usage

```bash
$ ansible-playbook playbooks/vmware_vm_create.yml -i inventories/foo -l bar
```

------

## History

| 2022/06/23 | 1.0.0 | initial release                                           |
