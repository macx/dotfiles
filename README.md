## Installation

## Prequisites

```shell
# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Configure Shell

I'm using the interactive [Zsh](https://www.zsh.org/) (Z Shell) as my daily driver instead of Bash and [Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh/wiki) to configure it to my needs. Install and configure both:

```shell
brew install zsh zsh-completions
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

#### Set Zsh as the defautl shell

- For your Terminal type:
  ```shell
  chsh -s /bin/zsh
  ```
- In Visual Studio Code open the command palette (CMD + P) and type `open settings json`. Choose "Open Settings (JSON) and add the following:
  ```json
  "terminal.integrated.defaultProfile.osx": "zsh",
  "terminal.integrated.profiles.osx": {
    "zsh": {
      "path": "/bin/zsh",
      "args": ["-l"],
      "icon": "terminal",
      "color": "terminal.ansiYellow"
    }
  },
  ```

```shell
$ brew install fontforge
```

### Shell

```shell
// Install tweeked fonts
$ brew tap homebrew/cask-fonts
$ brew install --cask font-hack-nerd-font
```
