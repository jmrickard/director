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
under_host_public: 'undercloud.redhat.public' 
undercloud_dns: 'undercloud.redhat.dns'
undercloud_node_dns: 'undercloud.redhat.dns1'
overcloud_domain_name: 'overcloud.redhat.local'
external_ip:
fdqn:
fdqn_short:
gen_cert: 'True'
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
under_glance_pass: 'underglance'
undercloud_heat_encryption_key: 'key'
undercloud_heat_pass: 'underheat'
undercloud_neutron_pass: 'underneutron'
undercloud_nova_pass: 'undernova'
undercloud_iron_pass: 'underpass'
undercloud_ceilometer_pass: 'underceilometer'
undercloud_aodh_pass: 'underaodh'
undercloud_sense_pass: 'undersensus'
undercloud_ceilometer_metering_secret: 'secret'
undercloud_ceilometer_snmpd_user: 'redhat'
undercloud_ceilometer_snmpd_pass: 'redhat'
undercloud_swift_passw: 'redhat'
undercloud_mistral_passw: 'mistral'
under_rabbit_cookie: 'cookie'
undercloud_rabbit_passw: 'rabbitpass'
undercloud_rabbit_username: 'rabbit'
undercloud_heat_stack_domain_admin_password: 'heatstackdomain'
undercloud_swift_hash_suffix: 'suffix'

under_monitoring: 'True'
novajoin: 'True'
undercloud_ipa_otp: 'redhat'
undercloud_docker_registry:
undercloud_db_password: 'redhat'
undercloud_admin_token: ''



defaults
stack_user: stack
stack_group: stack
stack_passwd: redhat
sudoer_perm: 0440
req_rpm: python-tripleoclient,git
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
