Role Name
=========

Super usefull role to change banners on Cisco Routers

Requirements
------------

You need to have a cisco router

Role Variables
--------------

```
text: "Put you banner here" 
```

Dependencies
------------

Not really

Example Playbook
----------------

Just include role in your playbook: 
```
- name: test
  hosts: iosxr01
  gather_facts: no
  connection: network_cli
  collections:
    - bgptelecom.cisco_collection

  tasks:
    - import_role:
        name: configure_banner
      vars:
        text: "This is EVE-NG Router! Generated {{ time }}"
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
