# ad-hoc commands

For actions quick prefer used ad-hoc commands, this is used modules.

## Test connection

Tests sample on inventory used ad-hoc commands

test of connection with module ping.

```bash
ansible --inventory=inventory.yml sede -m ping

ansible --inventory=inventory.yml parana -m ping
```

## Facts

Facts more details [here](https://docs.ansible.com/ansible/latest/user_guide/playbooks_vars_facts.html)

```bash

ansible --inventory=inventory.yml sede -m setup

ansible --inventory=inventory.yml sede -m setup >> rel.json

ansible --inventory=inventory.yml sede -m setup -a "filter=ansible_all_ipv4_addresses"

ansible --inventory=inventory.yml sede -m setup -a "filter=ansible_mounts"

ansible --inventory=inventory.yml sede -m setup -a "filter=ansible_interfaces"

ansible --inventory=inventory.yml sede -m setup -a "filter=ansible_distribution_release"

ansible --inventory=inventory.yml sede -m setup -a "filter=ansible_memfree_mb"

ansible --inventory=inventory.yml sede -m setup -a "filter=ansible_distribution_version"

ansible --inventory=inventory.yml sede -m setup -a "filter=ansible_os_family"

ansible --inventory=inventory.yml sede -m setup -a "filter=ansible_memory_mb"

```

## Manager packages

### Install packages

```bash



```

### Remove packages

```bash



```


## Manager groups

### Create

```bash



```

### Remove

```bash



```

### Change 

```bash



```



## Manager users

### Create

```bash



```

### Remove

```bash



```

### Change 

```bash



```




## Manager files and folders

### Create

```bash



```

### Remove

```bash



```

### Change 

```bash



```

## Manager services

### Create

```bash



```

### Remove

```bash



```

### Change 

```bash



```

## Manager firewall

### Create

```bash



```

### Remove

```bash



```

### Change 

```bash



```

## Manger network 

### Create

```bash



```

### Remove

```bash



```

### Change 

```bash



```



