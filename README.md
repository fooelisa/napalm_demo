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

### IP Interface config

* Generate ip interface config
```
ansible-playbook -i hosts playbooks/generate-interfaces-ip-config.yml
```

* Commit merge the ip interface configuration
```
ansible-playbook -i hosts playbooks/commit-merge-interfaces-ip-config.yml
```

### BGP config

* Generate BGP config
```
ansible-playbook -i hosts playbooks/generate-bgp-config.yml
```

* Commit merge the BGP configuration
```
ansible-playbook -i hosts playbooks/commit-merge-bgp-config.yml
```

### Now let's push them all at once

* Generate all configs
```
ansible-playbook -i hosts playbooks/generate-all-config.yml
```

* Commit merge all configs
```
ansible-playbook -i hosts playbooks/commit-merge-all-config.yml
```


### Retreive BGP session info

* Get BGP data
```
ansible-playbook -i hosts playbooks/get-bgp-data.yml
```
