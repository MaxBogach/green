# About

This repository contains everything you need for setup personal home server named "green". 
Server intends to be storage for private data and to be developer machine.

Repository consist of `Ansible playbooks` and `Docker-compose`

Ansible playbooks:
* check and config `sshd`
* install `docker-compose`
* clone this repository
* start/stop containers

Docker-compose
* samba
* github
* nexus
* teamcity