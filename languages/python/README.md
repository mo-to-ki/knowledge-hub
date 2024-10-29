# python-settings
目次

- [python-settings](#python-settings)
  - [pyenv](#pyenv)
  - [pip](#pip)
  - [venv](#venv)


## pyenv
* pyenv  
pythonのバージョン管理ツール。  
brewでインストールして、パスを通すことで使用することがでる。

* install  
pythonを任意のバージョンでダウンロードし、使用可能な状態にすることができる。
```shell
pyenv install 3.x.x
```
* install --list  
pyenvでダウンロード可能なpythonのバージョンを全て確認する。
```shell
pyenv install --list
```

* versions  
使用可能なpythonのバージョンを表示する。
```shell
pyenv versions
```

* global  
グローバルで使用されるpythonのバージョンの設定を行う。  
```shell
pyenv global python-version
```

* local  
ローカルで使用されるpythonのバージョンの設定を行う。  
```shell
pyenv local python-version
```

* --unset  
設定したpythonのバージョンの指定を解除する。  
```shell
pyenv {local or global} --unset
```

## pip
* install  
pythonのpackageをインストールする。


## venv
* venv  
仮想環境を作成する。  
```shell
python -m venv {env-name}
```

* 仮想環境の起動  
```shell
source ./env-name/bin/activate
```

* 仮想環境の停止  
```shell
source ./env_name/Scripts/deactivate
```

* ディレクトリ構造  
パッケージは以下のディレクトリに保存される。
```
./lib/{python-version}/site-packages
```
