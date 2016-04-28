OULibraries.centos7
=========

SSH Broker role for OULib.

Requirements
------------

A target system running CentOS7x.

Role Variables
--------------
hosts_allow contains entries for /etc/hosts.allow, eg.
```
hosts_allow:
  - comment: 'Some IP range'
    service: 'sshd'
    ip: '192.168.0.0/16'
```

Need usernames for the whitelist in the 'users' var. eg.

```
users:
  - name: 'centos'
    groups: 'wheel'
    pubkey: 'ssh-rsa somepubkey centos@example.org'
  - name: 'centos1'
    groups: 'wheel'
    pubkey: 'ssh-rsa anotherpubkey centos@example.org'
```

Dependencies
------------

Example Playbook
----------------

License
-------

To be determined

Author Information
------------------

Jason Sherman
