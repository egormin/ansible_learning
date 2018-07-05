Show ansible version
```
ansible --version
```

Show different parametres of VM
```
ansible tomcat_vm -i inventory -m setup   
## tomcat_vm - may be host name, or host group name or name rgoup of groups
```

To launch playbook
```
ansible-playbook site.yml -i inventory
```

To launch playbook (verbose mode)
```
ansible-playbook site.yml -i inventory -v
```

To check syntax
```
ansible-playbook site.yml -i inventory --syntax-check
```

Dry run
```
ansible-playbook site.yml -i inventory --check
```
Start without password. We can define only user name in inventory `ansible_ssh_user=vagrant` and ansible will ask the password if we use the key `-k`:
```
ansible-playbook site.yml -i inventory -k
```
