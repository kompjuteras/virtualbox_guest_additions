virtualbox_guest_additions
=========

Ansible role for the installation of the latest VirtualBox Guest Additions, with no need for the local media. Currently supported on:
- CentOS 6, 7, 8
- RedHat 6, 7, 8

Requirements
------------

Ansible server:
- Ansible 2.7+

Target machine(s):
- SSH connection and root (or sudo) access
- Internet access
- Package repositories are already configured and in use

Role Variables
--------------

File: defaults/main.yml
  - reboot_is_allowed (default: false)

Dependencies
------------

Of course, machine needs to be installed under VirtualBox

Example Playbook
----------------
Install the role
```
ansible-galaxy install kompjuteras.virtualbox_guest_additions --force
```

Playbook example
```
- name: Setup VirtualBox Guest Additions Tools
  hosts: all
  become: yes
  become_user: root
  become_method: sudo
  gather_facts: true
  ignore_errors: no

  roles:
     - kompjuteras.virtualbox_guest_additions
```

License
-------

GNU GPLv3

Author Information
------------------

Darko Drazovic \
LinkedIn: https://www.linkedin.com/in/darkodrazovic \
Personal: https://darkodrazovic.in.rs \
Blog: https://kompjuteras.com \
GitHub: https://github.com/kompjuteras
