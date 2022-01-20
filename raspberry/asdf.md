# asdf

https://asdf-vm.com/guide/getting-started.html

## Download

`git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.9.0`

## Install

```sh
echo '. $HOME/.asdf/asdf.sh' >> ~/.zshrc
```

## Configurations

configuration file `$HOME/.asdfrc`

supports `.nvmrc` and `.node-version` files.
```
legacy_version_file = yes
```

## Plugins

```sh
asdf plugin add nodejs
asdf plugin list
```

## Usage

```sh
asdf install nodejs latest (or 16.3.2)

asdf global nodejs latest
cat $HOME/.tool-versions

asdf local nodejs latest
cat $PWD/.tool-versions
```

