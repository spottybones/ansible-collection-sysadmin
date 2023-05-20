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

None.

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
