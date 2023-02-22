# Poetry

Lets run ansible from virtual environment.

Poetry may seem a bit heavy for simple task like this, but anyway.

### Install poetry

https://python-poetry.org/docs/#installing-with-the-official-installer

`curl -sSL https://install.python-poetry.org | python3 -`

`echo export PATH='$PATH:$HOME/.local/bin' >> $HOME/.bashrc`
`. $HOME/.bashrc`

`poetry completions bash > ${BASH_COMPLETION_USER_DIR:-${XDG_DATA_HOME:-$HOME/.local/share}/bash-completion}/completions/poetry`

### Fix completion for poetry

https://github.com/python-poetry/cleo/issues/133

Fix two-words commands with double quotes: `("command subcommand")`

### Install deps

`poetry install`

### Enter shell

`poetry shell`

Now we have ansible inside poetry shell.

# Ansible

### Lets get completions for ansible too.

Ansible uses python's argcomplete.

Argcomplete generates bash completion for all python scripts that use argparse.

Enable global argcomplete's completion for current user

`activate-global-python-argcomplete --dest=${BASH_COMPLETION_USER_DIR:-${XDG_DATA_HOME:-$HOME/.local/share}/bash-completion}/completions`

The trick here is to fed it with correct bash-completion directory.

### Run playbook

`ansible-playbook main.yml -K`

`-K` ask for privilege escalation password
