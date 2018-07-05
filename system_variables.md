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
