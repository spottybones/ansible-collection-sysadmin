common_packages
===============

This role installs software packages used by other roles in this
collection.

Requirements
------------

None.

Role Variables
--------------

The following role variables are supported:

    common_packages: [] # a LIST of packages to be installed

Supplied variables are OS dependent via separate include_vars files
in  the role's "vars" directory. The list defined in vars/debian.yml
includes:

    common_packages:
      - avahi-daemon
      - needrestart

Dependencies
------------

This role depends on roles in the ansible.builtin collection.

Example Playbook
----------------

Including an example of how to use your role (for instance, with
variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: spottybones.sysadmin.common_packages

License
-------

MIT

Author Information
------------------

Scott Burns <scott@cipher23.com>
