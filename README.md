# Ansible
Contains Ansible Playbook and tutorial notes and study guide

What is Ansible?
    - IT automation, configuration management and provisioning tools
    - It uses 'playbooks' to deploy, manage, build, test and configure anything from full server environments to websites to custom complied source code for application

Why Ansible?
    - Provisioning
    - Configuration Management
    - Continouns Delivery
    - Application Deployment
    - Security Compliance
    - Scripts

Ansible Features
    - Agentless: no need for agent installation and management
    - Built on top of python and hence provide a lot of python's functionality
    - Uses SSH for secure connections to servers
    - Follow push based architecture for sending configurations
    - Very easy and fast to setup, minimal requirements.

Push Based VS Pull Based
    - Tools like puppet and Chef are pull based, and agents need to be installed on each server/node that periodically checks for the configuration information from central server (master)
    - Ansible is push based, you control when the changes are made on the server/node by running the playbooks manually.

Ansible Use Case

Case 1:

![use_case_1](https://user-images.githubusercontent.com/101114171/215788946-0f54ea7f-3a8f-44e8-9802-c65323222461.png)
 
Case 2:

![use_case_2](https://user-images.githubusercontent.com/101114171/215789024-5c27f4c8-3580-48ec-80c9-1cf5f42d6cf5.png)

How Ansible Works:

![ansible_works](https://user-images.githubusercontent.com/101114171/215789104-a01748fa-cd69-4d4b-9b31-3d641c706dd3.jpg)
 
Ansible Management Node:
    Is the system where ansible is installed and all playbooks and inventory is kept

Inventory:
    Is the list of servers of host where ansible needs to make changes, manage for various automation nd configuration management tasks.
    Default location of host inventory is /etc/ansible/hosts but you can specify a different location with -i flag or the ansible.cfg configuration file.

Playbook:
    Contains the configuration/changes that you want to perform on each host

N/B: Ansible uses SSH to access the host to apply changes

Ansible Modules:
    - Modules also referred as task plugins or library plugins ar ethe ones which actually get executed inside a playbook
    - These are scripts that come packages with Ansible and perform some kind of action on a host
    Example:
        - apt: installs or removes packages using the apt package manager
        - copy: copies a file from local machine to the host
        - file: sets the attribute of a file, symlink or directory
        - service: starts, stops or restarts a service

Ansible AD_HOC Commands
    - An Ad-hoc command is something that you might type in to do something really quick but don't want to save for later.
    Example:
        - ansible all -s -n shell -a 'date'
        - ansible all -s -n shell -a 'service sshd status'

Ansible Playbook
    - Ansible's configuration, deployment and orchestration language is called ansible playbook
    - its written in YAML, declaratively define your configs. 
    - Human-readable and are developed in a basic text language
    -Command to run the playbook
        ansible-playbook file.yaml



