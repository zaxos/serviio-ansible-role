[![Build Status](https://travis-ci.org/zaxos/serviio-ansible-role.svg?branch=master)](https://travis-ci.org/zaxos/serviio-ansible-role)

serviio-ansible-role
===================

Ansible role to install Serviio Media Streaming Server.

Requirements
------------
centos 7, ansible >=1.6

Example Playbook
----------------
```
    - hosts: servers
      vars:
        serviio_version: 1.8
      roles:
         - role: serviio_ansible_role
```
