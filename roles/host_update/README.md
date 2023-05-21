spottybones.sysadmin.host_update
================================

Update the target host using that host's package manager and reboot
if necessary to complete the update.

Requirements
------------

This role uses anbible.builtin modules.

Role Variables
--------------

None.

Dependencies
------------

This role assumes that spottybones.sysadmin.common_packages has
been run to ensure the "needrestart" package is installed (on Debian
based distros.)

Example Playbook
----------------

Sample playbook follows:

    ---
    # vim:ft yaml.ansible
    - name: Update Hosts
      hosts: all
      roles:
        - role: spottybones.sysadmin.host_update

License
-------

MIT

Author Information
------------------

Scott Burns <scott@cipher23.com>
