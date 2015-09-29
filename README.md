openssh
=========

Ansible role to configure sshd on a remote host

Requirements
------------

None.

Role Variables
--------------

These are the defaults:

```yaml
# these are the setting I could want to change, but I leave them as defaults.
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

Dependencies
------------

None.

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: archf.openssh }
```

License
-------

BSD

Author Information
------------------

Felix Archambault
