ad_auth
=======

Role which helps to configure AD authentication.


Example
-------

```
---

# Default usage
- hosts: myhost1
  vars:
    # You will need yur own sssd config
    # (see: https://fedorahosted.org/sssd/wiki/Configuring_sssd_with_ad_server)
    sssd_config:
      ...
  roles:
    - ad_auth
```


Role variables
--------------

List of variables used by the role:

```
# Default authconfig options
ad_auth_authconfig_options:
  - "--enablesssd"
  - "--enablesssdauth"
  - "--enablemkhomedir"
  - "--enablelocauthorize"
  - "--update"
  - "--nostart"
```


Dependencies
------------

* [nsswitch](https://github.com/picotrading/ansible-nsswitch)
* [oddjob](https://github.com/picotrading/ansible-oddjob)
* [sssd](https://github.com/picotrading/ansible-sssd)


License
-------

MIT


Author
------

Jiri Tyr
