# Python_build_environment
pyenvとpipenvを使ったpythonの開発環境構築(備忘録)

## 環境
* macOS Mojave 
* Homebrew 2.1.16
* pyenv 1.2.15
* pipenv version 2018.11.26


## 手順

### pyenvの導入

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
terminalで実行
```
$ source ~/.bash_profile
$ pyenv install list
$ pyenv install 3.x.x
```

普段使用するPythonを設定する
```
$ pyenv global 3.x.x
```

### pipenvの使用法
pipenvのインストール
```
$ pip install pipenv
```
プロジェクトの初期化
```
$ pipenv --python 3.x
```
パッケージのインストール
```
$ pipenv install numpy
```
Pipfileから環境を再現する
```
$ pipenv install
```

## メモ
```
To activate this project's virtualenv, run pipenv shell.
Alternatively, run a command inside the virtualenv with pipenv run.
```
` $ pipenv shell `を実行するとpipenvの環境に入る.

pipenv環境の外から環境にアクセスするには` pipenv run `をコマンドの先頭につけて実行する.

## 参考サイト

[MacOSとHomebrewとpyenvで快適python環境を。](https://qiita.com/crankcube@github/items/15f06b32ec56736fc43a)

[Pipenvを使ったPython開発まとめ](https://qiita.com/y-tsutsu/items/54c10e0b2c6b565c887a)
