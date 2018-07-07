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
***Hostname:***
```
ansible_hostname: "first"
```
***Kernel version:***
```
ansible_kernel: "3.10.0-862.2.3.el7.x86_64"
```
***Total RAM amount:***
```
ansible_memory_mb.real.total: "512"
```
***OS family:***
```
ansible_os_family: "RedHat"
```
***Packet manager:***
```
ansible_pkg_mgr: "yum"
```
***Service manager:***
```
ansible_service_mgr: "systemd"
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
### Filtering facts
```
ansible -m setup -i inventory first -a filter="ansible_service_mgr"
```
### Create own facts:
Create file `/etc/ansible/facts.d/preferences.fact` with content:
```
[general]
eg=1
megatomcat='/opt/apache/tomcat'
```
To see our facts:
```
ansible -m setup -i inventory first -a filter="ansible_local"
```
