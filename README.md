# My Ansible Playbooks for DigitalOcean Droplets

## Usage

```bash
git clone git@github.com:Danand/ansible-digitalocean.git
cd ansible-digitalocean
venv-init # Depends on: git@github.com:Danand/bash-alias-sync.git
ansible-playbook -u root -i <ip-address-of-droplet>, droplet-ubuntu-22.04.yml
```
