spottybones.sysadmin.set_an_ansible_user
========================================

This role creates and user account on the target host with "sudo"
permission and is intended to serve as the host's ansible_user.

NOTE: "ansible_user" is a common ansible variable so we use
"an_ansible_user" (etc) to name variables unique to this role.

Requirements
------------

None.

Role Variables
--------------

The following role variables are supported:

    an_ansible_user
    an_ansible_user_comment
    an_ansible_user_ssh_authorized_key

Defaults are set in the defaults/main.yml file as follows:

    ---
    # defaults file for set_an_ansible_user
    an_ansible_user: ansible
    an_ansible_user_comment: Ansible User
    an_ansible_user_ssh_authorized_key: ''

WARNING: Make sure to supply a valid SSH public key for
"an_ansible_user_ssh_authorized_key" in group_vars or host_vars,
otherwise the new account will not be accessible.

Dependencies
------------

This role requires the installation of the ansible.posix collection,
which supplies the ansible.posix.authoried_key module.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: spottbones.sysadmin.set_an_ansible_user

License
-------

MIT

Author Information
------------------

Scott Burns, Cipher23 LLC
