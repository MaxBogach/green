About
=====

This repository contains everything you need for setup personal home server named "green". 
Server intends to be storage for private data and to be developer machine.

Repository consist of `Ansible playbooks` and `Docker-compose`

Ansible playbooks:
* ping server
* check and config `sshd`
* install `docker-compose`
* clone this repository
* start/stop containers

Docker-compose
* samba
* github
* nexus
* teamcity


How to use
==========
File `ansible/hosts` store IP address of server
```shell
cd ansible                            # All ansible's files store here
ansible-playbook playbook_ping.yml    # Jast ping server
```

