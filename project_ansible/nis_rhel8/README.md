# nis


## Files and Folders

mkdir nis_rhel8
touch inventory.yml playbook.yml README.md

mkdir -vp roles
cd roles/

ansible-galaxy init master
mkdir -vp master/files

ansible-galaxy init auxiliary
mkdir -vp auxiliary/files

ansible-galaxy init nfs
mkdir -vp nfs/files

ansible-galaxy init clients
mkdir -vp clients/files


## inventory

Tests sample on inventory used ad-hoc commands

test of connection with module ping.

```bash
ansible --inventory=inventory.yml sede -m ping --ask-become-pass
ansible --inventory=inventory.yml parana -m ping --ask-become-pass
```

Install new package on hosts of groups sede and parana

```bash
ansible --inventory=inventory.yml sede -m yum -a "name=curl state=present" --ask-become-pass
ansible --inventory=inventory.yml parana -m yum -a "name=curl state=present" --ask-become-pass
```

Other example with shutdow on sede in 2 minutes

```bash
ansible --inventory=inventory.yml sede -m shell -a "shutdown -h 2" --ask-become-pass
```
