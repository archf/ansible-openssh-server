ansible-openssh-servers
=======================

Ansible role to configure sshd on a remote host

Requirements
------------

None.

Role Variables
--------------

These are the defaults:

```yaml
sshd_config:
  PermitRootLogin: yes
  ChallengeResponseAuthentication: no
  GSSAPICleanupCredentials: no
  X11Forwarding: yes
  ClientAliveInterval: 0
  ClientAliveCountMax: 3
  PasswordAuthentication: yes
  Banner: 'none'
```

Those are implemeted directly in the jinja template.

Dependencies
------------

None.

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: archf.openssh-server }
```

License
-------

BSD

Author Information
------------------

Felix Archambault
