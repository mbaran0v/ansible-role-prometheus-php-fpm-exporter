# Ansible role: prometheus-php-fpm-exporter

[![Build Status](https://travis-ci.com/mbaran0v/ansible-role-prometheus-php-fpm-exporter.svg?branch=master)](https://travis-ci.com/mbaran0v/ansible-role-prometheus-php-fpm-exporter) [![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT) [![GitHub tag](https://img.shields.io/github/tag/mbaran0v/ansible-role-prometheus-nginxlog-exporter.svg)](https://github.com/mbaran0v/ansible-role-prometheus-php-fpm-exporter/tags/) [![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

Ansible role for install and configure [Prometheus PHP-FPM Exporter](https://github.com/bakins/php-fpm-exporter). Currently this works on Debian and RedHat based linux systems. Tested platforms are:

* Ubuntu 16.04
* CentOS 7

Requirements
------------

No special requirements; note that this role requires root access, so either run it in a playbook with a global become: yes

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows. (For all variables, take a look at defaults/main.yml)

```yaml
phpfpm_exporter_version: 0.6.1
```
version for installation

```yaml
phpfpm_exporter_listen_address: 0.0.0.0
phpfpm_exporter_listen_port: 8080
```
listen address and port

```yaml
phpfpm_exporter_root_dir: /opt/phpfpm_exporter
```
directory for installation

```yaml
phpfpm_exporter_http_endpoint: http://127.0.0.1:9000/status
```
HTTP endpoint in your webserver. Example for nginx: https://easyengine.io/tutorials/php/fpm-status-page/


Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: app
  become: yes
  roles:
      - mbaran0v.prometheus-php-fpm-exporter
```

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2019 by [Maxim Baranov](https://github.com/mbaran0v).
