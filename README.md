# Ansible

* Ansible is a Tool to automate IT Tasks like Configuration, Updates, Back-Ups and Reboots of Systems
* Also Tasks like create User, Assign Groups and Permissions
* It is Agent-less so only an SSH Connection is necessary to run Ansible on a remote Machine - Ansible has not to be
  installed on the remote Machine

 <p align="center">
    <img src="https://user-images.githubusercontent.com/29623199/136780885-3c1d78f8-7388-4c22-919e-7975b2b40941.JPG" alt="Ansible Agent-less" width="75%"/>
</P>

<hr>

## Advantages of Ansible

* Ansible executes Tasks from local Machine to remote Machines - instead of connecting into all remote Machines via SSH
* It allows to write all Steps for Configuration / Installation or Deployment in a single YAML-File - instead of running
  Shell Scripts
* It allows creating reusable Environments while using the same YAML-File multiple Times
* Ansible is more reliable and less likely for Errors - than Humans

<hr>

## Architecture of Ansible

### Ansible Modules

* Modules are provided by Ansible
* Modules are small Programs that do one specific Task - for Example: Install Ngnix Server or Start Docker Container
* Modules are sent (pushed) from the Control Machine to its Targets to do their Work and get removed
* Docker Module:

 <p align="center">
    <img src="https://user-images.githubusercontent.com/29623199/136781168-f29c819e-91bd-4943-96dd-c765e56dc161.JPG" alt="Ansible Docker Module" width="75%"/>
</P>

<hr>

### Ansible Playbook

* An Ansible Playbook consists of one or more Plays
* Each __Play__ contains of one or more __Tasks__
* Each __Task__ contains of one __Module__
* The Ansible Playbook executes multiple Modules in a Sequence from top to bottom - It orchestrates the Module Execution

 <p align="center">
    <img src="https://user-images.githubusercontent.com/29623199/136813844-683d0240-950b-4dea-99d6-5cb3b7a657e3.JPG" alt="Ansible Playbook" width="50%"/>
</P>

<hr>

### Ansible Inventory List

* The Inventory List contains the Hosts of the Playbooks - Configurations
* It contains all Machines that are involved in the Task Executions
* It allows building Groups so all Machines are affected - for example all Webservers

 <p align="center">
    <img src="https://user-images.githubusercontent.com/29623199/136814696-b2c50265-3fc7-4d1d-a6d0-59674b05080d.JPG" alt="Ansible Inventory" width="25%"/>
</P>
<hr>

### Ansible for Docker

* Ansible can be used as an Alternative to Dockerfile
* A Dockerfile packages an Application with all Configuration and Dependencies it needs
* Ansible can reproduce the Application across many Environments and not only for Docker Container

 <p align="center">
    <img src="https://user-images.githubusercontent.com/29623199/136816202-266f724b-d245-4753-8862-8ff7884bae3e.JPG" alt="Ansible for Docker" width="75%"/>
</P>
