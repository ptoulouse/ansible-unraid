# ansible-unraid

Using Ansible to deploy services to Unraid home server, whenever possible.

## Clone the repository

Clone the repository on your development computer using:

```bash
git clone https://github.com/ptoulouse/ansible-unraid.git
```

## Initial setup

Install a Git pre-commit hook that will ensure you are not committing an
unencrypted vault to the github repository. This hook checks for
*group_vars/\*/vault.yml* and *host_vars/\*/vault.yml*.

```bash
make gitinit
```

Setup the development environment:

* Create a Python virtual environment.
* Install pip packages.
* Install Galaxy requirements.

```bash
make setup
```

Set an ansible vault password in file *.vaultpass*.

## Other Makefile Commands

You can encrypt the vaults with ```make encrypt```.

You can decrypt the vaults with ```make decrypt```.

You can run ansible lint and syntax check to validate your code with
```make lint```.

You can run the ansible playbook *playbook.yml* with ```make deploy```.
