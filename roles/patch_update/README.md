Patch Update
=========

This is a simple proof of concept role to update a server using yum.  The role uses a block format to run a rescue task to add any failed server to an aggregated list using set_stats module.  If the yum update is successful the server will be added to the succeeded list.  The intent is to construct the roles in a Workflow template in Ansible Tower.  The second role, patch_report, will take the JSON data from the set_stats module and email it in YAML format.

Requirements
------------

Ansible Tower
Workflow design

Role Variables
--------------

**Default Variables**
```
report_failed: []
report_success: []
```

Dependencies
------------

Ansible Tower

Example Playbook
----------------

    - hosts: all
      gather_facts: false
      tasks:
        - name: Import the patch update role
          import_role:
            name: patch_update

License
-------

BSD

Author Information
------------------

John Best <jbest@redhat.com>
