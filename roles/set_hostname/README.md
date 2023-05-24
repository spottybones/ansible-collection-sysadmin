spottybones.sysadmin.set_hostname
=================================

This role will set the host's hostname using systemctl/hostnamectl.
It will also update the /etc/hosts file and set "preserve_hostname"
to "true" for hosts with cloud-init installed.

Requirements
------------

None

Role Variables
--------------

| Variable              | Type   | Default            | Purpose                                    |
| --------------------- | ------ | ------------------ | ------------------------------------------ |
| set_hostname_hostname | string | {{ ansible_host }} | allow customization of hostname if desired |

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: spottybones.sysadmin.set_hostname }

License
-------

MIT

Author Information
------------------

* Scott Burns, Cipher23 LLC
