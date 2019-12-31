# Ansible

Example of how to use Ansible

## Install Ansible on Ubuntu 18.04.3 LTS (Controlling Machine)

jmendoza@jmendoza-ThinkPad-T420:~$ sudo apt-get update

jmendoza@jmendoza-ThinkPad-T420:~$ sudo apt-get upgrade -y

jmendoza@jmendoza-ThinkPad-T420:~$ sudo reboot

jmendoza@jmendoza-ThinkPad-T420:~$ sudo apt-add-repository ppa:ansible/ansible

jmendoza@jmendoza-ThinkPad-T420:~$ sudo apt-get update

jmendoza@jmendoza-ThinkPad-T420:~$ sudo apt-get install ansible -y

![Screenshot](/Prtsc/Ansible_1.png)

## Ansible Inventory

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

### File: Tasks.yml

![Screenshot](/Prtsc/Ansible_10.1.png)

jmendoza@jmendoza-ThinkPad-T420:~/IdeaProjects/Ansible/Playbook$ ansible-playbook Tasks.yml -K

![Screenshot](/Prtsc/Ansible_10.png)

### File: Nginx.yml

![Screenshot](/Prtsc/Ansible_11.png)

![Screenshot](/Prtsc/Ansible_11.1.png)

jmendoza@jmendoza-ThinkPad-T420:~/IdeaProjects/Ansible/Playbook$ ansible-playbook Nginx.yml -K

![Screenshot](/Prtsc/Ansible_11.2.png)

![Screenshot](/Prtsc/Ansible_11.3.png)