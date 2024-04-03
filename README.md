`dimmaryanto93.haproxy`
=========

This ansible role to help you install HAProxy for supported platform:

- CentOS 7/8
- Oracle Linux 8.7
- Ubuntu 20.04

Requirements
------------

Untuk menggunakan role ini, kita membutuhkan package/collection

- [ansible.posix](https://github.com/ansible-collections/ansible.posix)

Temen-temen bisa install, dengan cara

```bash
ansible-galaxy collection install ansible.posix --force
```

Atau temen-temen bisa menggunakan `requirement.yaml` file and install menggunakan `ansible-galaxy collection install -r requirement.yaml`, dengan format seperti berikut:

```yaml
---
collections:
  - ansible.posix
```

Role Variables
--------------

Ada beberapa variable yang temen-temen bisa gunakan untuk setting docker daemon, diantaranya seperti berikut:

| Variable name                    | Example value  | Description |
| :---                             | :---           | :---        |
| `haproxy_version`                | `*1.8.27*`     | Install specific version, if you want install latest keep it blank |


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- name: Install HAProxy loadbalancer
  hosts: ['all']
  become: true
  roles: 
    - dimmaryanto93.haproxy
```

License
-------

MIT

