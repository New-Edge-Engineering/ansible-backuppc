# Ansible BackupPC Role #

Ansible role to install and configure BackupPC. Feedback, bug-reports, requests,
is welcomed and can be done via
[github issues](https://github.com/New-Edge-Engineering/ansible-ansible/issues).

## Requirements & Dependencies ##
- Tested on Mac OS X with Ansible 1.5.
- Tested on Ubuntu Precise with Ansible 2.2.1.0

## Variables ##
see defaults/main.yml for variables to overwrite and their explainations

Example role include:
```
vars:
  - backuppc_url: 'http://some.domain.tld'
  - backuppc_hosts: [
     { name: 'some.host.tld', os: 'linux', type: 'rsync' }
     { name: 'other.host.tld', os: 'linux', type: 'rsync' }
   ]
 - backuppc_users: [ 
     { name: 'backuppc', pass: 'secret' }
   ]
 - backuppc_manage_hosts: yes
 
roles:
  - backuppc

    }
```

## Tests ##
You can test this role by using the provided Vagrant file in ./tests

```bash
bacuppc/tests$ vagrant up <os>
bacuppc/tests$ vagrant ssh <os>
```

For <os>, you can choose:
* ubuntu-trusty
* ubuntu-boinic
* centos7 

## License ##

Licensed under the MIT License. See the LICENSE file for details.
