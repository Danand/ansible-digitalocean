# My Ansible Playbooks for DigitalOcean Droplets

## Usage

### Set up

```bash
git clone git@github.com:Danand/ansible-digitalocean.git
cd ansible-digitalocean
venv-init # Depends on: git@github.com:Danand/bash-alias-sync.git
```

### Install essential dependencies

```bash
ansible-playbook \
  -u root \
  -i <ip-address-of-droplet>, \
  droplet-ubuntu-22.04.yml
```

### Run `certbot`

```bash
ansible-playbook \
  -u root \
  -i <ip-address-of-droplet>, \
  certbot-dns.yml \
  -e 'domain=<domain-name>' \
  -e 'email=<owner-email>'
```
