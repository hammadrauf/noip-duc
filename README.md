# Ansible Role: noipduc

Forked from: [Mot93 - noip duc client for RPi](https://github.com/Mot93/rpi-install-noip-dynamic-update-client)

This role installs the NOIP.com dynamic update client, and launches it as a service. For Debian and RHEL based OSes.

The role follows the [official guide](https://www.noip.com/support/knowledgebase/install-linux-3-x-dynamic-update-client-duc#install_from_source).


## Requirements
None


### Default variables

```
tar_version: "3.1.0"
noip_username: "noip_user"
noip_password: "password"
noip_domain_names:
  - abc.com
  - xyz.ca
noip_check_interval: "900s"
```

### Vars variable
```
tar_version: "3.1.0"
noip_username: "noip_user"
noip_password: "password"
noip_domain_names:
  - abc.com
  - xyz.ca
noip_check_interval: "900s"
```

## Dependencies
None

## Example Playbook
Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
    - hosts: servers
      become: true
      tasks:
        - import_role:
            name: hammadrauf.noipduc
          vars:
            noip_username: "noip_user"
            noip_password: "password"
            noip_domain_names:
            - abc.com
```

## License
MIT

## Authors
- Mattia Rubini
- Hammad Rauf

