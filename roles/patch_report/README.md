Patch Update
=========

This is a simple proof of concept role to report the status of a yum update.  The role uses the mail module to send an email constructed with data from the set_stats module from the patch_update role.  It is designed to be the second template in an Ansible Tower workflow template.  It will pass the JSON variables report_failed and report_success into the email body in YAML (to_nice_yaml) format.

Requirements
------------

Ansible Tower
Workflow design

Role Variables
--------------

**Default Variables**
```
report_failed: []  | **This should be overriden from the patch_update role**
report_success: []  | **This should be overriden from the patch_update role**
```

**Required Variables**
```
report_mailhost: nameofmailhost.domain.com
report_mailport: 25
report_mailto: Recipient <username@domain.com>
report_mailfrom: Sender <username@domain.com>
```

Dependencies
------------

Ansible Tower

Example Playbook
----------------

    - hosts: all
      gather_facts: false
      tasks:
        - name: Import the patch report role
          import_role:
            name: patch_report

License
-------

BSD

Author Information
------------------

John Best <jbest@redhat.com>
