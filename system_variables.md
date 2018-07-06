***To know host fqdn:***
```
ansible_fqdn: "ubuntu2.example.com"
```
***To know host OS architecture:***
```
ansible_userspace_architecture: "x86_64"
```
***To know OS:***
```
ansible_distribution: "CentOS"
```
***OS major version:***
```
ansible_distribution_major_version: "7"
```
***OS full version:***
```
ansible_distribution_version: "7.5.1804"
```
***Default IPv4 address:***
```
ansible_default_ipv4.address: "10.0.2.15"
To use:
- debug: var=ansible_default_ipv4.address
```
***Hostname from inventory file:***
```
ansible_nodename: "first"
```
***Get list of hosts in group:***
```
{{groups['DEV']}}
```
***Get host vars:***
```
{{hostvars['hostname']}}
```
***Get IP of the first host of group:***
```
{{hostvars[groups['DEV'][0]]['ansible_eth0']['ipv4']['address']}}
{{hostvars[groups['DEV'][0]].ansible_eth0.ipv4.address}}
```
