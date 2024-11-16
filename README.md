# Ansible Playbook Template

A git repository template for getting started with Ansible.

## Using This Repository Template

The `ansible.cfg` file sets the location of the following files

- `private_key_file = ~/.ssh/ansible`
- `vault_password_file = ~/.ansible/vault-pass.txt`

### Private Key File

`private_key_file` sets the default location of the ansible user SSH private key
to access the remote host

### Vault Password File

`vault_password_file` sets the location of the ansible password for encrypting and
and decrypting vaults. This stores the password in plain text and should be outside
of your repository with the appropriate file permissions set. This allows encrypted 
vaults to be stored in the repository without exposing the secrets.

## Repository Structure

This repository is put together with the following structure
