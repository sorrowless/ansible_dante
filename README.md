sbog/dante
==========

Role to install and configure Dante socks4/5 server

#### Requirements

Ansible 2.4

#### Role Variables

```yaml
# Configuration actually just repeats dante config, so read dante documentation
# first to understand what all these fields really mean
danted:
  logoutput: /var/log/danted.log
  internal_name: "{{ ansible_default_ipv4.interface }}"
  internal_port: 1027
  external: "{{ ansible_default_ipv4.interface }}"
  clientmethod: none
  method: none
  user:
    privileged: root
    notprivileged: nobody
    libwrap: nobody
  client:
    pass:
      first_client_pass:
        - "from: 0.0.0.0/0 to: 0.0.0.0/0"
  pass:
    first_pass:
      - "from: 0.0.0.0/0 to: 0.0.0.0/0"
```

#### Dependencies

None

#### Example Playbook

```yaml
- name: Install Dante proxy to target servers
  hosts: dante
  remote_user: root

  roles:
    - { role: dante, tags: ['dante'] }
```

#### License

Apache 2.0

#### Author Information

Stanislaw Bogatkin (https://sbog.ru)
