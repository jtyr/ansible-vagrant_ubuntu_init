vagrant_ubuntu_init
===================

Ansible role which helps to install all necessary to run Ansible on an Ubuntu
Vagrant box.


Usage
-----

```
- name: Example of basic usage of this role
  # This is important otherwise the first run will fail
  gather_facts: no
  hosts: all
  roles:
    - vagrant_ubuntu_init
```


Role variables
--------------

```
# Expected path for the Python executable
vagrant_ubuntu_init_path: /usr/bin/python

# Python package name
vagrant_ubuntu_init_pkg: python-minimal

# Command to run to install Python
vagrant_ubuntu_init_cmd: apt -y update && apt install -y {{ vagrant_ubuntu_init_pkg }}
```


License
-------

MIT


Author
------

Jiri Tyr
