# INSTALL `pyenv`

Homebrew:

```sh
brew update
brew install pyenv
```

## Set Up Shell Environment

[https://github.com/pyenv/pyenv#set-up-your-shell-environment-for-pyenv]

Most reliable way to get pyenv in all environments is to append pyenv configuration commands to both `.bashrc` (for interactive shells) and profile file (for login shells). Similarly for zsh.

```sh
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
```
