# Ansible Role: ansible-apps_nginxlog_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_nginxlog_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_nginxlog_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__nginxlog_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_nginxlog_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_nginxlog_exporter/tags)

Deploy [nginxlog_exporter](https://github.com/martin-helmich/prometheus-nginxlog-exporter/) to expose nginxlog metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `nginxlog_exporter_version` | 1.7.1 | nginxlog_exporter version |
| `nginxlog_exporter_upgrade` | false | force upgrade |
| `nginxlog_exporter_listen_address` | 127.0.0.1 | address to listen |
| `nginxlog_exporter_listen_port` | 9109 | port to expose prometheus metrics |

## Examples

	---
	- hosts: apps_nginxlog_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_nginxlog_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
