inmotionhosting.apache
=========

Modular Ansible Role for deploying and configuring Apache

[![Build Status](https://travis-ci.org/inmotionhosting/ansible-role-apache.png?branch=master)](https://travis-ci.org/inmotionhosting/ansible-role-apache)

Requirements
------------

* CentOS 7.x or later
* Debian 9 or later
* Ubuntu 16.04.x LTS or later

Role Variables
--------------

| Variable | Description |
| -------- | ----------- |
| apache_name | Default: `httpd`
| apache_daemon | Default: `httpd`
| apache_user | Default: `apache`
| apache_group | Default: `apache`
| apache_port | Default: `80`
| apache_secure_port | Default: `443`
| apache_config | Default: `/etc/{{ apache_name }}/conf/{{ apache_name }}.conf`
| apache_config_path | Default: `/etc/{{ apache_name }}/conf.d`
| apache_config_ports | Default: `{{ apache_config_path }}/ssl.conf`
| apache_config_site_path | Default: `{{ apache_config_path }}`
| apache_modules_path | Default: `/etc/{{ apache_name }}/modules`
| apache_modules_config_path | Default: `/etc/{{ apache_name }}/conf.modules.d`
| apache_packages | The list of Apache packages to install

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: www
      roles:
         - role: inmotionhosting.apache

License
-------

GPLv3

Author Information
------------------

[InMotion Hosting](https://inmotionhosting.com)
