Patch Update
=========

This is a simple proof of concept role to update a server using yum.  The role uses a block format to run a rescue task to add any failed server to an aggregated list using set_stats module.  The intent is to construct the roles in a Workflow template in Ansible Tower.  The second role, patch_report, will take the JSON data from the set_stats module and email it in YAML format.

Requirements
------------

Ansible Tower
Workflow design

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
