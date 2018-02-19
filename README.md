Role Name
=========

This role allows you to install salt-minion from the latest salt repo

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

just take a look at defaults.yml

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

```yaml
---
- hosts: [test20180219]
  become: yes
  vars:
    salt_config:
      master: somemaster.domain.org
      retry_dns: 30
      master_port: 4506
      conf_file: /etc/salt/minion
      random_startup_delay: 1
      hash_type: sha512
      keysize: 8192
      log_file: /dev/null
      log_level: critical
  roles:
    - salt_minion
...
```

License
-------

BSD

Author Information
------------------

Stanislav Cherkasov 
adm@tenhi.ru
