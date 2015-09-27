# N.A.P.A.L.M. + Ansible Demo

### Base config

To init the router with its base config, basic configuration tasks need to be performed beforehand. The demo routers need to be set up with connectivity and access credentials. This is mostly meant to clear the config for demo purposes.

* Generate intial config
```
ansible-playbook -i hosts playbooks/generate-init-config.yml
```

* Commit replace initial config
```
ansible-playbook -i hosts playbooks/commit-replace-init-config.yml
```

### System config

* Merge more system config into the existing base
```
ansible-playbook -i hosts playbooks/generate-system-config.yml
```

* Commit merge the system configuration
```
ansible-playbook -i hosts playbooks/commit-merge-system-config.yml
```
