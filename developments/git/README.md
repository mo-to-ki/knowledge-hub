# git-command

目次
- [git-command](#git-command)
  - [brach](#brach)
  - [fetch](#fetch)
  - [merge](#merge)
  - [clone](#clone)
  - [reset](#reset)
  - [show](#show)
  - [rebase](#rebase)
  - [diff](#diff)
  - [config](#config)
  - [reflog](#reflog)
  - [stash](#stash)

## brach

* branch  
現在のブランチをもとに、新規ブランチを作成する。
```shell
git branch {new-branch}
```

## fetch
* fetch  
リモートブランチをローカルにダウンロードする。
```shell
git fetch origin
```

## merge
* merge  
任意のブランチを現在のブランチに読み込む。
```shell
git merge {merge-branch}
```

## clone
* clone  
リモートリポジトリをローカルにダウンロードする。
```shell
git clone https://{user-name}:{token}@github.com/username/repo.git
```

## reset
* reset  
n個のコミットを削除する。

  * --soft  
ワーキングエリアとステージングエリアには情報を保持する。  

  * --mixed  
ワーキングエリアには情報を保持する。  

  * --hard  
付随情報を含めて全て削除する。
```shell
git reset --soft HEAD~{n}
```

## show
* show  
コミットの変更内容を表示する。
```shell
git show
```

## rebase
* rebase  
n個のコミットを結合する。  
```shell
git rebase -i HEAD~{n}
```

## diff
* diff  
編集内容の確認
```shell
git diff
```

## config
* config  
認証設定ファイルを編集する。  
```shell
git config --local --edit
```


## reflog
* reflog  
過去の操作の表示、巻き戻しができる。
```shell
git reflog
# 99698e4 HEAD@{0}: commit: 0
# 7c53a64 HEAD@{1}: commit: 1
# 46bde33 HEAD@{2}: commit: 2
# 1e04a9a HEAD@{3}: commit: 3
# 05f755f HEAD@{4}: commit: 4
# 5cddd0e HEAD@{5}: commit: 5
```
* reset HEAD@{n}  
任意の操作まで巻き戻す。
```shell
git reset HEAD@{2}
```

## stash
* stash  
コミットしていない編集内容をステージングエリアから外して保存する。
```shell
git stash -m "message"
```
* list  
保存してあるスタッシュを確認する。
```shell
git stash list
# stash@{0}: stash: 0
# stash@{1}: stash: 1
# stash@{2}: stash: 2
# stash@{3}: stash: 3
```
* pop  
保存してあるスタッシュを適用して削除
```shell
git stash pop stash@{0}
```

* apply  
保存してあるスタッシュを適用
```shell
git stash apply stash@{0}
```

* drop  
保存してあるスタッシュの削除
```shell
git stash drop stash@{0}
```
