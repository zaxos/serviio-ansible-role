[![Build Status](https://travis-ci.org/zaxos/serviio-ansible-role.svg?branch=master)](https://travis-ci.org/zaxos/serviio-ansible-role)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-_zaxos.serviio--ansible--role-blue.svg)](https://galaxy.ansible.com/zaxos/serviio-ansible-role/)

serviio-ansible-role
====================

Ansible role to install Serviio Media Streaming Server.

Requirements
------------
* centos/rhel 7 or ubuntu 16.04
* ansible >= 2.2
* selinux disabled

Installation
------------
```
$ ansible-galaxy install zaxos.serviio-ansible-role
```

Example Playbook
----------------
```yaml
    - hosts: servers
      vars:
        serviio_version: 1.8
      roles:
        - role: zaxos.serviio-ansible-role
```

Role Variables
--------------
The main variable:
- `serviio_version`: serviio version to install (latest is 1.8)

Some variables that require review:
- `serviio_configure_firewalld`: True   
By default firewalld will be installed, configured and enabled if CentOS/RedHat operating system is detected. Change to "False" if you don't want to use firewalld.
- `serviio_install_path`: /opt

Some defaults (probably not requiring tampering):
- `serviio_download_URL`: http://<i></i>download.serviio.org/releases
- `serviio_user`: serviio
- `serviio_group`: serviio
- `serviio_create_service`: True
- `serviio_service_name`: serviio
- `serviio_enabled_on_startup`: True
- `serviio_start_service_after_install`: True

Usage
-----
After installation, point your browser to: `http://IP_or_FQDN:23423/console`
