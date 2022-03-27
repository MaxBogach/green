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
* TODO: start/stop containers

Docker-compose
* samba
* TODO: github
* TODO: nexus
* TODO: teamcity


How to use
==========
Config files (make copy from *.sample file): 
* `ansible/hosts` store IP address of server
* `.env` store username and password for samba share `Storage`
```shell
ansible-galaxy collection install community.docker

cd ansible                            # All ansible's files store here
cp hosts.sample hosts                 # Make copy of server config
nano hosts                            # Set configuration variables. This file ignored by git
ansible-playbook playbook_00_ping.yml                       # Jast ping server
ansible-playbook playbook_01_config_sshd.yml                # Disable password authentication
ansible-playbook playbook_02_install_docker_compose.yml     # Install Docker-Compose
ansible-playbook playbook_03_clone_repository.yml           # Clone repository to server
ansible-playbook playbook_04_start_docker-compose.yml       
ansible-playbook playbook_05_stop_docker-compose.yml
```
