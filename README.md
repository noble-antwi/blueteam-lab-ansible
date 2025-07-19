# blueteam-lab-ansible

This is the stage where i get to the Ansible Stage to automate my Lab 

## Obtain Information about one Host

```bash
ansible  all -m gather_facts --limit 192.168.60.2


```

## Obtain Information on all hosts


```bash
ansible  all -m gather_facts -
```