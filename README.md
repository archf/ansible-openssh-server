ansible-openssh-servers
=======================

Ansible role to configure sshd on a remote host

Requirements
------------

None.

Role Variables
--------------

These are the values you can change and also the defaults:

```yaml
sshd_config:
  Port: 22
  PermitRootLogin: 'yes'
  ChallengeResponseAuthentication: 'no'
  GSSAPICleanupCredentials: 'no'
  X11Forwarding: 'yes'
  ClientAliveInterval: 0
  ClientAliveCountMax: 3
  PasswordAuthentication: 'yes'
  Banner: 'none'
```

To override, create a `sshd_config` with dictionary key/value pairs as show above.
You do not need to list the keys you do not want to change.

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

MIT

Author Information
------------------

Felix Archambault
