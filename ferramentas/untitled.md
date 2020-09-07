# Como instalar e usar ASDF na WLS 2

```text
sudo apt update
sudo apt install build-essential git automake autoconf libreadline-dev libncurses-dev libssl-dev libyaml-dev libxslt-dev libffi-dev libtool unixodbc-dev unzip curl zlib1g-dev sqlite3 libsqlite3-dev

git clone https://github.com/asdf-vm/asdf.git ~/.asdf
cd ~/.asdf
git checkout "$(git describe --abbrev=0 --tags)"
```

## if you are using oh-my-zsh \(you should\)

```text
echo -e '\n. \$HOME/.asdf/asdf.sh' >> ~/.zshrc
source ~/.zshrc
```

## else

```text
echo -e '\n. $HOME/.asdf/asdf.sh' >> ~/.bashrc
echo -e '\n. $HOME/.asdf/completions/asdf.bash' >> ~/.bashrc
source ~/.bashrc
```

## end

```text
asdf --version
```

## install ruby

```text
asdf plugin-add ruby
asdf install ruby 2.7.1
asdf global ruby 2.7.1
ruby -v
```

## install node

```text
asdf plugin-add nodejs
bash ~/.asdf/plugins/nodejs/bin/import-release-team-keyring
asdf install nodejs 12.17.0
asdf global nodejs 12.17.0
node -v
```

