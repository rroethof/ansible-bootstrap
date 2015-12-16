Ansible bootstrap a new server
==============================

Bootstrapping a new server using ansible.


Requirements
------------

 * RHEL 6/7
 * CentOS 6/7
 * Ubuntu 13/14/15


Role Variables
--------------

```
reboot: true
```


Dependencies
------------

This role is not dependend on any, but can co-excist with i.e. network-interfaces


Example Playbook
----------------

```yaml
- hosts: all
  user: root
  become: true
  serial: 1
  vars:
    - reboot: true
  roles:
    - { role: network-interfaces }
    - { role: bootstrap }
```


License
-------

GPLv3


Author Information
------------------

Ronny Roethof
