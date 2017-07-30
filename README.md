Mongodb Ansible
==========

This role installs mongodb on the host machines.

Requirements
------------

The control machine SSH key must be on the `authorized_keys` of the DB server machine. To install mongodb, sudo access is required hence the `become: true` in `prep-demo.yml`.

Role Variables
--------------

- `mongodb_ver`: The version of mongodb you want to install
- `os_family`: The os family of your host machine, see (https://repo.mongodb.org/yum/) for the choices.
- `os_version`: The os version of your host machine. (e.g: '7' for RHEL 7)

Running the Playbook
--------------------

`$ ansible-playbook playbooks/mongodb-ansible.yml --ask-become-pass`
