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

test of connection with module ping and shell.

*module ping*

```bash
ansible --inventory=inventory.yml sede -m ping

ansible --inventory=inventory.yml parana -m ping
```

*module shell show files*

```bash
ansible --inventory=inventory.yml sede -m shell -a "cat /etc/redhat-release"
```

*module shell copy files*

```bash
ansible --inventory=inventory.yml sede -m shell -a "cp /etc/redhat-release /etc/redhat_bkp"
```

*module setup for get reports*

```bash
ansible --inventory=inventory.yml sede -m setup >> rel.json
```


Install new package on hosts of groups sede and parana

*module yum*

```bash
ansible --inventory=inventory.yml sede -m yum -a "name=curl state=present" --ask-become-pass
ansible --inventory=inventory.yml parana -m yum -a "name=curl state=present" --ask-become-pass
```

*module package*

```bash
ansible --inventory=inventory.yml sede -m package -a "name=htop state=present" --ask-become-pass
ansible --inventory=inventory.yml sede -m package -a "name=htop state=absent" --ask-become-pass
```

Other example with shutdow on sede in 2 minutes

```bash
ansible --inventory=inventory.yml sede -m shell -a "shutdown -h 2" --ask-become-pass
```
