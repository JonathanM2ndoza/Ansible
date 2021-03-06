# Ansible

Ansible is a software tool that provides simple but powerful automation for cross-platform computer support. It is primarily intended for IT professionals, who use it for application deployment, updates on workstations and servers, cloud provisioning, configuration management, intra-service orchestration, and nearly anything a systems administrator does on a weekly or daily basis.

![Screenshot](/Prtsc/Ansible_intro1.png)

# Ansible Architecture

![Screenshot](/Prtsc/Ansible_intro2.png)


## Install Ansible on Ubuntu 18.04.3 LTS (Controlling Machine)

jmendoza@jmendoza-ThinkPad-T420:~$ sudo apt-get update

jmendoza@jmendoza-ThinkPad-T420:~$ sudo apt-get upgrade -y

jmendoza@jmendoza-ThinkPad-T420:~$ sudo reboot

jmendoza@jmendoza-ThinkPad-T420:~$ sudo apt-add-repository ppa:ansible/ansible

jmendoza@jmendoza-ThinkPad-T420:~$ sudo apt-get update

jmendoza@jmendoza-ThinkPad-T420:~$ sudo apt-get install ansible -y

![Screenshot](/Prtsc/Ansible_1.png)

## Ansible Inventory: Part One

Add your host in /etc/ansible/hosts 

jmendoza@jmendoza-ThinkPad-T420:~$ sudo vim /etc/ansible/hosts 

![Screenshot](/Prtsc/Ansible_2.png)

### Configure your host to access with ssh (Managed Node)

For help see file [commands.txt](commands.txt)

![Screenshot](/Prtsc/Ansible_3.png)

jmendoza@jmendoza-ThinkPad-T420:~$ docker inspect ubuntu

![Screenshot](/Prtsc/Ansible_4.png)

![Screenshot](/Prtsc/Ansible_5.1.png)

### Configure your user to access with ssh (Managed Node)

jmendoza@jmendoza-ThinkPad-T420:~$ sudo vim /etc/ansible/ansible.cfg 

![Screenshot](/Prtsc/Ansible_6.png)

## Ansible ad-hoc command 

![Screenshot](/Prtsc/Ansible_7.1.png)

![Screenshot](/Prtsc/Ansible_8.png)

### Install VIM in Managed Node

![Screenshot](/Prtsc/Ansible_9.png)

jmendoza@jmendoza-ThinkPad-T420:~$ ansible 172.17.0.2 -m apt -a 'name=vim state=present' -b -K

![Screenshot](/Prtsc/Ansible_9.1.png)

![Screenshot](/Prtsc/Ansible_9.2.png)

![Screenshot](/Prtsc/Ansible_9.3.png)

![Screenshot](/Prtsc/Ansible_9.4.png)

![Screenshot](/Prtsc/Ansible_9.5.png)

## Ansible Playbooks

### Example 1: Tasks.yml

![Screenshot](/Prtsc/Ansible_10.1.png)

jmendoza@jmendoza-ThinkPad-T420:~/IdeaProjects/Ansible/Playbook$ ansible-playbook Tasks.yml -K

![Screenshot](/Prtsc/Ansible_10.png)

### Example 2: Nginx.yml

![Screenshot](/Prtsc/Ansible_11.png)

![Screenshot](/Prtsc/Ansible_11.1.png)

jmendoza@jmendoza-ThinkPad-T420:~/IdeaProjects/Ansible/Playbook$ ansible-playbook Nginx.yml -K

![Screenshot](/Prtsc/Ansible_11.2.png)

![Screenshot](/Prtsc/Ansible_11.3.png)

### Example 3: Apache2.yml - Handlers

hosts: 172.17.0.2 

![Screenshot](/Prtsc/Ansible_12.png)

![Screenshot](/Prtsc/Ansible_12.1.png)

jmendoza@jmendoza-ThinkPad-T420:~/IdeaProjects/Ansible/Playbook$ ansible-playbook Apache2.yml -K

![Screenshot](/Prtsc/Ansible_12.2.png)

hosts: 172.17.0.2 

![Screenshot](/Prtsc/Ansible_12.3.png)

![Screenshot](/Prtsc/Ansible_12.4.png)

## Ansible Inventory: Part Two

jmendoza@jmendoza-ThinkPad-T420:/etc/ansible$ vim servers 

![Screenshot](/Prtsc/Ansible_13.png)

![Screenshot](/Prtsc/Ansible_13.1.png)

jmendoza@jmendoza-ThinkPad-T420:/etc/ansible$ vim servers

![Screenshot](/Prtsc/Ansible_13.2.png)

![Screenshot](/Prtsc/Ansible_13.3.png)