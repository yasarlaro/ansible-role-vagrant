Role Name
=========

This role installs vagrant on `Centos 7`,  `Centos 8`, or `Ubuntu 18` servers. The expected vagrant provider is either `VirtualBox` or `libvirt`.

Requirements
------------

One of the below virtualization software needs to be installed on the supported operating systems:
- KVM
- VirtualBox

If you would like to install the hypervisor, you can refer to either my [KVM](https://galaxy.ansible.com/yasarlaro/kvm) or [VirtualBox](https://galaxy.ansible.com/yasarlaro/virtualbox) role.

Role Variables
--------------

The role expects to provide one of the supported virtualization software to `default_provider` variable. The expected values are:
- libvirt (default)
- virtualbox

Dependencies
------------

The hypervisor needs to be installed on the supported servers. You can refer to either my [KVM](https://galaxy.ansible.com/yasarlaro/kvm) or [VirtualBox](https://galaxy.ansible.com/yasarlaro/virtualbox) role.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
    - hosts: servers
      become: yes
      roles:
         - { role: yasarlaro.kvm, libvirt_user: "onur" }
         - { role: ansible-role-vagrant, default_provider: "libvirt" }
```

License
-------

MIT

