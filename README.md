<H3>Ansible Roles:</H3>

<b>defaults</b>
```
Role default variables. Lowest priority.
main.yml
```
<b>files</b>
```
Role resources for “copy” module
```
<b>handlers</b>
```
Role handlers
main.yml
```
<b>meta</b>
```
Role dependencies
main.yml
```
<b>tasks</b>
```
Role tasks
main.yml
```
<b>templates</b>
```
Role resources for “template” module
```
<b>vars</b>
```
Role variables. Stronger priority then defaults
main.yml
```
<b>library</b>
```
Modules
```
<b>tests</b>
```
Role unit tests
inventory
test.yml
```
### Roles parameters:
```
roles:
- common                  # without parameters
- role: tomcat_install    # with parameters
  app_port: 9000
  app_dir: '/opt'
```
or we can write:
```
roles:
- common                 
- { role: tomcat_install, app_port: 9000, app_dir: '/opt'}
```

### Remark:
We should use "{{ var }}" after module or parameter name (after :). For example:
```
- service
  - name: "{{ var }}"
```
in order avoid considering by ansible as it is yaml structure. In this case we don't need " ":
```
  tasks:
  - name: copy to {{ var }}
```
### playbook.retry:
This file contains hostname of host where occurs last fail


