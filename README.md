# N.A.P.A.L.M. + Ansible Demo

### Base config

To init the router with its base config, basic connectivity needs to be established beforehand. The demo routers will need to be set up and have a basic setup. This is meant to clear the config for demo purposes.

* Generate intial config
```
ansible-playbook -i hosts playbooks/generate-init-config.yml
```

* Commit replace initial config
```
ansible-playbook -i hosts playbooks/commit-replace-init-config.yml
```

### Deploy config

This will generate the various config snippets (roles), merge them and upload them to the devices. The following roles are available in this demo:
..*base-config
..*system
..*interfaces


* Batch deploy all available roles
```
ansible-playbook -i hosts playbooks/generate-config.yml
```

* Commit the complete configuration
```
ansible-playbook -i hosts playbooks/commit-config.yml
```
