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

* Generate more system config
```
ansible-playbook -i hosts playbooks/generate-system-config.yml
```

* Commit merge the system configuration
```
ansible-playbook -i hosts playbooks/commit-merge-system-config.yml
```

### Interface config

* Generate interface config
```
ansible-playbook -i hosts playbooks/generate-interface-config.yml
```

* Commit merge the interface configuration
```
ansible-playbook -i hosts playbooks/commit-merge-interface-config.yml
```

### OSPF config

* Generate ospf config
```
ansible-playbook -i hosts playbooks/generate-ospf-config.yml
```

* Commit merge the ospf configuration
```
ansible-playbook -i hosts playbooks/commit-merge-ospf-config.yml
```
