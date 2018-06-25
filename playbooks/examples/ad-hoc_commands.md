### AD-HOC COMMANDS
They use for single, quick operations.

Common syntax is next:
```
ansible host_or_group -m modile -a "arguments" [-i inventory]
```
If we use command without `-m module` module `shell` will be used.

### Examples:
Get facts info. If we skip `-i inventory` will be used file `/etc/ansible/hosts`.
```
ansible remote_host -m setup
```
Get info of some parameter:
```
ansible first -m setup -a 'filter=ansible_os_family' -i inventory
```
Get date of local host:
```
ansible localhost -a date
```
