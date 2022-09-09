## Poetry - python environment

1. Install poetry

https://python-poetry.org/docs/#installing-with-the-official-installer
`curl -sSL https://install.python-poetry.org | python3 -`
`export PATH="$PATH:$HOME/.local/bin"`
`poetry completions bash > ${BASH_COMPLETION_USER_DIR:-${XDG_DATA_HOME:-$HOME/.local/share}/bash-completion}/completions/poetry`

2. Fix completion for poetry

https://github.com/python-poetry/cleo/issues/133
Fix two-words commands with double quotes: `("command subcommand")`

3. Install deps

`poetry install`

4. Enter shell

`poetry shell`

Now we have ansible inside poetry shell.


## Ansible

1. Lets get completions for ansible too.

Ansible uses python's argcomplete. 
Argcomplete generates bash completion for all python scripts that use argparse.
Enable global argcomplete's completion for current user

`activate-global-python-argcomplete --dest=${BASH_COMPLETION_USER_DIR:-${XDG_DATA_HOME:-$HOME/.local/share}/bash-completion}/completions`

The trick here is to fed it with correct bash-completion directory.

2. Run playbook

`ansible-playbook main.yml -K`

`-K` ask for privilege escalation password
