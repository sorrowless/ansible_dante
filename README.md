# sbog/dante

[![Build Status](https://travis-ci.com/sorrowless/ansible_dante.svg?branch=master)](https://travis-ci.com/sorrowless/ansible_dante)
[![Ansible Role](https://img.shields.io/ansible/role/25790)](https://galaxy.ansible.com/sorrowless/dante)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/25790)](https://galaxy.ansible.com/sorrowless/dante)
[![Ansible Role](https://img.shields.io/ansible/role/d/25790)](https://galaxy.ansible.com/sorrowless/dante)
[![GitHub](https://img.shields.io/github/license/sorrowless/ansible_dante)](https://github.com/sorrowless/ansible_dante/blob/master/LICENSE)

Role to install and configure Dante socks4/5 server

## Requirements

Ansible 2.4

## Role Variables

Look for these at `defaults/main.yml` file.

## Dependencies

None

## Example Playbook

```yaml
- name: Install Dante proxy to target servers
  hosts: dante
  remote_user: root

  roles:
    - { role: dante, tags: ['dante'] }
```

## License

Apache 2.0

## Author Information

This role was created by [Stan Bogatkin](https://sbog.ru).
