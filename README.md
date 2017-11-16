Role Name
=========
Install all the requirements and undercloud.

Requirements
------------


Role Variables
--------------
---
```

this is a quick group_vars that can be used for prod/dev. A more indept templated undercloud.conf file can be found in templates/undercloud.conf.j2.test

group_vars
```
under_image: '/home/stack/images/' 
under_host: 'undercloud.redhat.local' 
ip_add: '192.168.10.28/24'
gateway: '192.168.10.254' 
public_vip: '132.250.80.28' 
admin_vip: '192.168.10.253' 
gen_serv_cert: 'True' 
local_int: 'eth1' 
gen_ca: 'local' 
cidr: '192.168.10.0/24' 
masquerade: '192.168.10.0/24'
dhcp1: '192.168.10.50' 
dhcp2: '192.168.10.100' 
ins_interface: 'br-ctlplane' 
ins_iprange: '192.168.10.200,192.168.10.250' 
ins_runbench: 'False' 
ins_enable_uefi: 'True' 
under_debug: 'False' 
tempest: 'False' 
mistral: 'True' 
zaqar: 'True' 
telemetry: 'True' 
on_ui: 'True' 
en_valid: 'True' 
ipxe_en: 'True' 
events: 'False' 
cl_nodes: 'False' 
under_admin_pass: 'undercloud'

defaults
stack_user: stack
stack_group: stack
stack_passwd: redhat
sudoer_perm: 0440
req_rpm: python-tripleoclient,git,mariadb-server
external_ip: 192.168.5.5
fqdn: test.osp.redhat.com
fqdn_short: test.osp
```


Dependencies
------------


Example Playbook
----------------
---
  - hosts: all
    roles:
      - osp-director


License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
