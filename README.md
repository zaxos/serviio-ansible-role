[![Build Status](https://travis-ci.org/zaxos/serviio-ansible-role.svg?branch=master)](https://travis-ci.org/zaxos/serviio-ansible-role)

serviio-ansible-role
===================

Ansible role to install Serviio Media Streaming Server.

Requirements
------------
centos 7, ansible >=1.6, selinux disabled

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
         - role: zaxos.serviio_ansible_role
```

Role Variables
--------------
The main variable:
- `serviio_version`: serviio version to install (latest is 1.8)

Some defaults (probably not requiring tampering)
- `serviio_download_URL`: http://<i></i>download.serviio.org/releases
- `serviio_install_java`: True
- `serviio_java_package`: "java-1.8.0-openjdk"
- `serviio_install_path`: /opt
- `serviio_user`: serviio
- `serviio_group`: serviio
- `serviio_create_service`: True
- `serviio_service_name`: serviio
- `serviio_enabled_on_startup`: True
- `serviio_start_service_after_install`: True
