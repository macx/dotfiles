# Prequisites

Install the Package manager [Homebrew](https://brew.sh/), if you haven't done it before.

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

I'm using the [Zsh](https://www.zsh.org/) (Z Shell) as my daily driver instead of Bash and [Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh/wiki) to configure it to my needs. Install and configure both:

```shell
brew install zsh zsh-completions
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Now, set Zsh as your default shell:

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

### Configure your Shell

```shell
brew install fontforge

# Install tweeked fonts
brew tap homebrew/cask-fonts
brew install --cask font-hack-nerd-font

# Install Powerlevel10k Theme
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc.`.
