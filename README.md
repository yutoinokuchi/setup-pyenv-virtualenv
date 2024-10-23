# pyenv-virtualenv (rather than Attention) Is All You Need

As far as I know, **pyenv-virtualenv** is the best Python version management tool.

Have you ever experienced any of these before?
- [ ] Conflict between pip and co*da in an environment.
- [ ] Forgot to change the environment with "co*da activate".
- [ ] When using pyenv, you want to create multiple virtual environments with a single Python version.

If any of these statements apply to you, I highly recommend pyenv-virtualenv.

> Source  
> pyenv : https://github.com/pyenv/pyenv  
> pyenv-virtualenv : https://github.com/pyenv/pyenv-virtualenv

## Installation
For **bash** (Linux):
1. pyenv
```
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
source ~/.bashrc
```

2. pyenv-virtualenv
```
git clone https://github.com/pyenv/pyenv-virtualenv.git $(pyenv root)/plugins/pyenv-virtualenv
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bashrc
source ~/.bashrc
```

For **zsh** (Mac):

0. update
```
brew update
```
1. pyenv
```
brew install pyenv
echo 'export PYENV_ROOT="${HOME}/.pyenv"' >> ~/.zshrc
echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="${PYENV_ROOT}/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
source ~/.zshrc
```

2. pyenv-virtualenv
```
brew install pyenv-virtualenv
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.zshrc
source ~/.zshrc
```

## Usage

### pyenv
1. Check installable Python versions first
```
pyenv install -l
```

2. Install a Python version
```
pyenv install <python-version>
```
> An example:
```
pyenv install 3.10.15
```

3. Check available Python versions
```
pyenv versions
```

4. Global setting
```
pyenv global <python-version>
```
> An example:
```
pyenv global 3.10.15
```

### pyenv-virtualenv
1. Create a virtual environment
```
pyenv virtualenv <python-version> <env-name>
```
> An example:
```
pyenv virtualenv 3.10.15 proX
```

2. Check the created virtual environment (just in case)
```
pyenv versions
```

3. Local setting
```
mkdir <project-dir>
cd <project-dir>
pyenv local <env-name>
```
> An example:
```
mkdir projectX
cd projectX
pyenv local proX
```

- Delete a virtual enviroment (if necessary):
```
pyenv uninstall <env-name>
```
