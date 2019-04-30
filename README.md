# Katuma secrets

DEPRECATED in favour of https://github.com/openfoodfoundation/ofn-secrets. See https://github.com/coopdevs/katuma_secrets/issues/11 for details.

These are the secrets files used for Katuma's staging and production environments.

## Usage

After cloning this repo you'll need to tell Ansible where the secrets are located and that it needs to ask you the password of the vault. You can do that as follows:

```shell
$ ansible-playbook playbooks/deploy.yml --limit es-staging --ask-vault-pass -e "@../katuma_secrets/staging.yml"
```

Note this makes use of Ansible's [--extra-vars](https://docs.ansible.com/ansible/latest/user_guide/playbooks_variables.html#passing-variables-on-the-command-line) argument. That's the mechanism to pass variables on the command line.
