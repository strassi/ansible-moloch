Role Name
=========

Moloch installation, which only covers MolochCapture and MolochViewer (subject to change)

Requirements
------------

The role requires a Ubuntu distribution and was tested with the following versions:
 - Ansible 2.9
 - Moloch 2.0.1-1
 - Ubuntu 18.04 

Role Variables
--------------

All of the roles variables are defined in `defaults/main.yml`

### `moloch_uninstall`
- Moloch can be uninstalled
- Default value: **false**

### `moloch_version`
- which version of moloch should be installed
- Default value: **2.0.1-1**

### `moloch_elasticsearch`
- hostname / ip of elasticsearch cluster
- Default value: **localhost**

### `moloch_interface`
- Capture interface
- Default value: **eth0**

## `moloch_bpf`
- BPF filter for capturing
- Default value: **None**

## `moloch_passwort_secret`
- S2S secrect for encryption of passwords in elasticsearch
- Default value: **defaultpassword**

## `moloch_admin_user`
- Default admin user for the viewer dashboard
- Default value: **admin**

## `moloch_admin_password`
- Default admin password for the viewer dashboard
- Default value: **admin**

Dependencies
------------

Ansible needs the following packagess on the target machine to deploy the role:
 - xz-utils
 - python3-pexpect

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: strassi.moloch }

License
-------

GPLv3

Author Information
------------------

