# What is this?

This is a simple playbook to set up a private Docker registry on a VPS.
I use it for my kamal deployments because I'm tired of clearing the DigitalOcean registry manually.

## Info

It is based on [registry image](https://hub.docker.com/r/library/registry) and there are [deployment instructions](https://distribution.github.io/distribution/about/deploying).

## Requirements

- [ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-and-upgrading-ansible)


## Setup

1. Copy the inventory file `cp inventory.example inventory`

2. Update the `inventory` file to include your VPS ipv4 address and path to the ssh key.

3. Copy the secrets file `cp vars/example_secrets.yml vars/secrets.yml`

4. Fill up the `secrets.yml` with your values.

## Run

```bash
ansible-playbook -i inventory ./playbook.yml
```
