# Tmux

Tmux é um multiplexador de terminal, ou seja ele permite você manipular as janelas de seu terminal de forma dinâmica.

{% embed url="https://github.com/tmux/tmux/wiki" %}

### Como Instalar:

```bash
sudo apt-get install tmux
```

### Configuração:

para configurar o Tmux é preciso editar o arquivo `~/.tmux.config`, porém ao instalar e utilizar o Tmux, este arquivo não é inicializado, para isso, vamos utilizar um arquivo de configuração disponibilizado pela comunidade em [https://github.com/gpakosz/.tmux](https://github.com/gpakosz/.tmux).

```bash
$ cd
$ git clone https://github.com/gpakosz/.tmux.git
$ ln -s -f .tmux/.tmux.conf
$ cp .tmux/.tmux.conf.local .
```

você pode editar o arquivo `~/.tmux.config` para adicionar novas configurações.  ``

#### Utilização de Mouse: 

```bash
set -g mouse on
bind -n WheelUpPane if-shell -F -t = "#{mouse_any_flag}" "send-keys -M" "if -Ft= '#{pane_in_mode}' 'send-keys -M' 'select-pane -t=; copy-mode -e; send-keys -M'"
bind -n WheelDownPane select-pane -t= \; send-keys -M
```

#### Desabilitar renomeação automática da janela:

```bash
set-window-option -g allow-rename off
set-window-option -g automatic-rename off
bind-key c new-window \; set-window-option -q allow-rename on \; set-window-option  -q automatic-rename on
```

### Links Uteis: 

{% embed url="https://github.com/rothgar/awesome-tmux" %}



