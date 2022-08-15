# Dotfiles @macx

Dotfiles are configuration files for varous programs on your computer, primarily recognizable by the beginning dot in the file name. This can resist per repository or system wide. This repository is my approach to sync these settings throughout different Mac-Installations.

## Installation

Run the following script to get this dotfiles installed on your system. It will backup your existing ones.

```shell
curl https://raw.githubusercontent.com/macx/dotfiles/main/scripts/config-init | bash
```

Please read the [Prequisites](./docs/prequisites.md) and follow it's instructoins to setup your maschine.

## Working with the Dotfiles

The Z Shell config sets up `dots` which is an alias to `git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME`.

This means you can use the following commands from any directory, and it will properly tracked in the repro at `~./.dotfiles`.

```shell
dots add ./path/to/file
dots commit -m "Add some file"
dots push
```

To get an update:

```shell
dots pull
```
