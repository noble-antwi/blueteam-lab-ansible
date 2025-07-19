# blueteam-lab-ansible

This is the stage where i get to the Ansible Stage to automate my Lab 

## Obtain Information about one Host

```bash
ansible  all -m gather_facts --limit 192.168.60.2


```

## Obtain Information on all hosts


```bash
ansible  all -m gather_facts 
```

## Ad Hoc Commands with Elevated Priviledges

### Update all Hosts Regardless of Opearting Systems
```bash
ansible all -m apt -a "update_cache=true"
```

### Updating only Ubnutu Hosts
```bash
ansible ubuntu -m apt -a "update_cache=true" --become --ask-become-pass
``

### Updating only Rocky Liniux(RHEL)nHosts

```bash
ansible rocky -m yum -a "update_cache=yes" -become --ask-become-pass
``

### Installing Pakcage on the Ubuntu Instances
```bash
ansible ubuntu -m apt -a name=vim-nox --become --ask-become-pass
```

```bash
ansible ubuntu -m apt -a name=tmux --become --ask-become-pass
```
```bash
sudo ansible ubuntu -m apt -a "name=snapd state=latest" --become --ask-become-pass
```


### Upgrdae all packages on Ubuntu
```bash
sudo ansible ubuntu -m apt -a "upgrade=dist" --become --ask-become-pass
```
