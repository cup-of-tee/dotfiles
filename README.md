# Dotfiles

Inspired by https://github.com/ALT-F4-LLC/dotfiles

# Packets

- nvim
- - TODO: git plugin
- - TODO: copy-paste plugin. make sure xclip & xsel are not used (disaster in wsl)
- - TODO: apt install python3-venv (for mason)
- mics
- - TODO: alias `grep --color=always` and `less -R` in .bashrc to preserve colors in less

# Prerequisites

- - openssh
- - gh
    `gh completion -s bash > ${BASH_COMPLETION_USER_DIR:-${XDG_DATA_HOME:-$HOME/.local/share}/bash-completion}/completions/gh`
