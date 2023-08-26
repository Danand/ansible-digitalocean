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
  -i ${ip_address_of_droplet}, \
  droplet-ubuntu-22.04.yml
```

### Run `certbot`

```bash
ansible-playbook \
  -u root \
  -i ${ip_address_of_droplet}, \
  certbot-dns.yml \
  -e "domain=${domain}" \
  -e "email=${email}"
```

### Install Knative CLI

```bash
ansible-playbook \
  -u root \
  -i ${ip_address_of_droplet}, \
  knative-cli.yml
```

### Install Kubernetes `kind`

```bash
ansible-playbook \
  -u root \
  -i ${ip_address_of_droplet}, \
  k8s-kind.yml
```

### Install Kubernetes `kubectl`

```bash
ansible-playbook \
  -u root \
  -i ${ip_address_of_droplet}, \
  k8s-kubectl.yml
```
