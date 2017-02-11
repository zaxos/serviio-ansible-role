[![Build Status](https://travis-ci.org/zaxos/serviio-ansible-role.svg?branch=master)](https://travis-ci.org/zaxos/serviio-ansible-role)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-%20zaxos.serviio--ansible--role-blue.svg)](https://galaxy.ansible.com/zaxos/serviio-ansible-role/)

serviio-ansible-role
===================

Ansible role to install Serviio Media Streaming Server.

Requirements
------------
* centos/rhel 7
* ansible >= 1.8
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

Some defaults (probably not requiring tampering):
- `serviio_download_URL`: http://<i></i>download.serviio.org/releases
- `serviio_java_package`: "java-1.8.0-openjdk"
- `serviio_install_path`: /opt
- `serviio_user`: serviio
- `serviio_group`: serviio
- `serviio_create_service`: True
- `serviio_service_name`: serviio
- `serviio_enabled_on_startup`: True
- `serviio_start_service_after_install`: True

Usage
-----
After installation, point your browser to: `http://IP_or_FQDN:23423/console`
