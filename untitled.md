# index

This is my collection of tools and environments configs.

## Environment

OS: Windows 10 Code: WSL2 - Ubuntu 18.04.4 LT

## Tools

### Terminal

#### Terminal Emulator:

[alacritty](https://github.com/alacritty/alacritty)

#### Shell:

[Zsh + Oh my Zsh!](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)

Active plugins:

```text
plugins=(git docker docker-compose ruby wd rake asdf bundler)
```

Aliases

```text
alias be="bundle exec"
```

**Plugins:**

Multiplex: [tmux](https://github.com/tmux/tmux/wiki) Project Launcher: [tmuxinator](https://github.com/tmuxinator/tmuxinator)

**Enable Mouse in Tmux:**

add this to `.tmux.conf`:

```text
# make mouse select and resize work
set -g mouse on
# make scrolling with wheels work
bind -n WheelUpPane if-shell -F -t = "#{mouse_any_flag}" "send-keys -M" "if -Ft= '#{pane_in_mode}' 'send-keys -M' 'select-pane -t=; copy-mode -e; send-keys -M'"
bind -n WheelDownPane select-pane -t= \; send-keys -M
```

#### Development Stack

### typescript

[https://react-typescript-cheatsheet.netlify.app/](https://react-typescript-cheatsheet.netlify.app/)

[https://basarat.gitbook.io/typescript/](https://basarat.gitbook.io/typescript/)

[https://github.com/TypeStrong/ts-node](https://github.com/TypeStrong/ts-node)

