# Python_build_environment
pyenvとpipenvを使ったpythonの環境構築(備忘録)

## 環境
* macOS Mojave 
* Homebrew 2.1.16
* pyenv 1.2.15
* pipenv version 2018.11.26


## 手順
terminalで実行
```
$ brew upgrade
$ brew install pyenv
```
.bash_profileに追記
```
export PYENV_ROOT=/usr/local/var/pyenv
if which pyenv > /dev/null; then eval "$(pyenv init -)"; fi
```
```
$ source ~/.bash_profile
$ pyenv install list
$ pyenv install 3.x.x
```
