# Git-Planning
Gitの利用方法

## 学習環境の設定
User直下にGit管理の学習フォルダ`learning`を作成し、`$ git init`  
⇒　特定のレポジトリに紐づかないGit環境の作成  

- 学習対象がGitHub上にレポジトリを有する場合  
  当該レポジトリをフォーク`Fork`  
  フォークしたレポジトリをローカルの学習用フォルダ`learning`にクローン  
  `$ git clone 対象のURL`  
  作成されたフォルダを学習対象に関するGitの作業フォルダにする
- 学習対象がGitHub上にレポジトリを有しない場合  
  GitHub上に新しい学習用のレポジトリを作成  
  作成したレポジトリをローカルの学習用フォルダ`learning`にクローン  
  `$ git clone 対象のURL`  
  作成されたフォルダを学習対象に関するGitの作業フォルダにする  

## リモートレポジトリの更新
1. ローカルリポジトリのインデックスに新規もしくは修正したファイルをステージング    
`$ git add ファイル名`  
`$ git add -A`  
1. 新規もしくは修正をコミット  
`$ git commit -m "コメント"`  
-m: コメントオプション  
1. リモートレポジトリに変更を反映  
`$ git push origin master`  

## ローカルレポジトリの更新
とりあえず下記で問題なさそう  
`$ git pull`  

## その他Gitコマンド
* 作業フォルダの状態確認  
`$ git status`  
* 作業フォルダに設定されているリモートレポジトリのURL確認  
`$ git remote -v`  

  
## 参考サイト
[GitのHEADとは何者なのか](https://qiita.com/ymzk-jp/items/00ff664da60c37458aaa)
