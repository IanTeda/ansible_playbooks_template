# Ansible Playbook Template

A git repository template for getting started with Ansible.

## Repository Structure

This repository is put together with the following structure

1. ansible.cfg
2. Host Inventory
3. Group Variables
4. Host Variables

## Ansible Config

The `ansible.cfg` file sets the location of the following files

- `inventory = ./inventory`
- `private_key_file = ~/.ssh/ansible`
- `vault_password_file = ~/.ansible/vault-pass.txt`

### Inventory

`inventory` sets the location of the host inventory files. This can be `.ini` or `.yaml`.
The inventory file can be one file or broken up. I like to break then up per host group.


### Private Key File

`private_key_file` sets the default location of the ansible user SSH private key
to access the remote host

### Vault Password File

`vault_password_file` sets the location of the ansible password for encrypting and
and decrypting vaults. This stores the password in plain text and should be outside
of your repository with the appropriate file permissions set. This allows encrypted 
vaults to be stored in the repository without exposing the secrets.

## Group Variables

`./group_vars` create a group variable for each inventory group. The 'all.yaml' 
can be used as a vault (encrypted) and or ignored.

## Host Variables

`./host_vars` create a host variable for each host in the inventory