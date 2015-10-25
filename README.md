# NAPALM + Ansible Demo

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

### VLAN config

* Generate VLAN config
```
ansible-playbook -i hosts playbooks/generate-vlan-config.yml
```

* Commit merge the VLAN configuration
```
ansible-playbook -i hosts playbooks/commit-merge-vlan-config.yml
```

### BB Interface config

* Generate BB interface config
```
ansible-playbook -i hosts playbooks/generate-interfaces-bb-config.yml
```

* Commit merge the BB interface configuration
```
ansible-playbook -i hosts playbooks/commit-merge-interfaces-bb-config.yml
```

### Customer Interface config

* Generate customer interface config
```
ansible-playbook -i hosts playbooks/generate-interfaces-cust-config.yml
```

* Commit merge the customer interface configuration
```
ansible-playbook -i hosts playbooks/commit-merge-interfaces-cust-config.yml
```
