inmotion.apache
=========

Modular Ansible Role for deploying and configuring Apache

[![Build Status](https://travis-ci.org/inmotionhosting/inmotion.apache.png?branch=master)](https://travis-ci.org/inmotionhosting/inmotion.apache)

Requirements
------------

* RHEL/CentOS 7.x, 8.x
* Debian 9.x, 10.x
* Ubuntu 16.04 LTS, 18.04 LTS

Role Variables
--------------

### Defaults
| Variable | Definition |
| -------- | ---------- |
| apache_user  | The user Apache will run as
| apache_group | The group the Apache user will be assigned to

### Vars
| Variable | Definition |
| -------- | ---------- |
| apache_name         | The name of the Apache package
| apache_daemon       | The name of the Apache service daemon
| apache_config       | The Full path and name of the Apache configuration file
| apache_config_path  | The path of the Apache configuration directory
| apache_modules_path | The path of the Apache modules directory
| apache_packages     | The packages to install for Apache

Dependencies
------------
None.

Example Playbook
----------------

    - hosts: www
      roles:
         - role: inmotion.apache

License
-------

GPLv3

Author Information
------------------

InMotion Hosting
