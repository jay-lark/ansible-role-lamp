Ansible-role-LAMP
=========

This Ansible role will install a configure a simple LAMP installation on a Debian/Ubuntu based server  

Requirements
------------

Other than a working Ansible installation noting extra is required for this role.

Role Variables
--------------

In vars/main.yml put your desired password for the MySQL root user.

Example Playbook
----------------

Put your MySQL root password in vars/main.yml, and use something like the following in your playbook.

    ---- 
    - 
      become: true
      hosts: all
      roles:
      - role: ansible-role-lamp

This role was primarily designed to used in deployments of new servers so it will first do an apt update && apt upgrade on the system.  It will then reboot the server if required.

License
-------

MIT


