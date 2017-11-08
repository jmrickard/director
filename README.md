# OSP Director


### Info

This playbook installs all the requirements needed for the undercloud. The undercloud config file is used as a template with the variables in group_vars/prod or dev. Initially only prod has the file but, we can create the dev file to follow the same format. The host that are going to be target need to have the group as prod or dev. Example:

```
[prod]
192.168.5.5


[dev]
osp-director.rh.fedora.com


