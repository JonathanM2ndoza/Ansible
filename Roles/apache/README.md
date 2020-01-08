Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).


Example Simple Role Apache
------------------

## 1: ansible-galaxy init apache --offline

![Screenshot](/Prtsc/Ansible_14.png)

## 2: create files for role apache

![Screenshot](/Prtsc/Ansible_14.1.png)

## 3: ansible-playbook site.yml --syntax-check

![Screenshot](/Prtsc/Ansible_14.2.png)

## 4: ansible-playbook site.yml

![Screenshot](/Prtsc/Ansible_14.3.png)

## 5: Service Apache status

![Screenshot](/Prtsc/Ansible_14.4.png)


