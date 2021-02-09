# ansible-role-dns
Ansible role to manage resolv.conf

## How to install
### requirements.yml
**Put the file in your roles directory**
```yaml
---
- src: https://github.com/adieperi/ansible-role-dns.git
  scm: git
  version: master
  name: ansible-role-dns
```
### Download the role
```Shell
ansible-galaxy install -f -r ./roles/requirements.yml --roles-path=./roles
```
## Exemple Playbook
```yaml
---
- hosts: all
  tasks:
    - name: Include ansible-role-dns
      include_role:
        name: ansible-role-dns
      vars:
        resolvNameServer:
          - 10.1.0.2
          - 190.12.4.67
          - 1.1.1.1
        resolvSearchDomain: domain.net
```
