# Windows User Authenticatie

This Ansible role configures RHEL systems to use Microsoft Active Directory authentication.

After performing this, it is possible to login with Local and Active Directory users.

## Requirements

Make sure the RHEL system has a hostname and the domain controller is added as an NTP server.
As well that the DNS settings are correct.

## Role variables

Look through all of the options in [defaults/main.yml](defaults/main.yml) and set the variables to reflect your needs. The options are described there in full detail.

## Playbook example

```sh
- hosts: localhost
  vars_files:
    - /root/adauth.yml

  roles:
     - windows-user-auth
```

In the `vars_files`, a variable file can be given that overwrites the default variables in the role.