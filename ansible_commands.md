Show ansible version
```
ansible --version
```

Show ansible version
```
ansible --version
```

Show different parametres of VM
```
ansible tomcat_vm -i inventory -m setup   ## tomcat_vm - may be host name, or host group name or name rgoup of groups
```

To launch playbook
```
ansible-playbook site.yml -i inventory
```

To launch playbook (verbose mode)
```
ansible-playbook site.yml -i inventory -v
```