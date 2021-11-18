# **Patching Report**
Playbooks to update servers and then report on success or failure of each server. They should be a part of an **Ansible Tower Workflow**. This is only a Proof of Concept solution currently.

## Ansible Tower Workflow
1. patch_update.yml - This playbook will import the [patch_update](https://github.com/tech2734/patching_report/tree/main/roles/patch_update) role, launch the patching update block which will track the success and failure status of each host being updated.  The data will be stored in an aggregated fact using the set_stats module


2. patch_report.yml - This playbook will import the [patch_report](https://github.com/tech2734/patching_report/tree/main/roles/patch_report) role which will email the results of the patch_update role to the intended recipient.

