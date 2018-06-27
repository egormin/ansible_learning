### Variables in Ansible
Ansible has 3 main scopes:
1. **Global** set in config, environment variables, command line vars
2. **Play** vars in playbooks, in role defaults and vars
3. **Host**: inventory, include vars, facts

#### Vars priority (from low to high):
- role defaults
- inventory file or script group vars (Variables defined in inventory file or provided by dynamic inventory)
- inventory group_vars/all
- playbook group_vars/all
- inventory group_vars/*
- playbook group_vars/*
- inventory file or script host vars
- inventory host_vars/*
- playbook host_vars/*
- host facts / cached set_facts
- inventory host_vars/*
- playbook host_vars/*
- host facts
- play vars
- play vars_prompt
- play vars_files
- role vars (defined in role/vars/main.yml)
- block vars (only for tasks in block)
- task vars (only for the task)
- include_vars
- set_facts / registered vars
- role (and include_role) params
- include params
- extra vars (always win precedence)
