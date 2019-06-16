# Git-Planning
Gitの利用方法

## 学習環境の設定
User直下にGit管理の学習フォルダ`learning`を作成し、`$ git init`  
⇒　特定のレポジトリに紐づかないGit環境の作成  

- 学習対象にGitHub上のレポジトリがある場合  
  当該レポジトリをフォーク`Fork`  
  このレポジトリを学習フォルダ`learning`にクローン  
  `$ git clone 対象のURL`  
  新しく出来たフォルダをGitの作業フォルダにする
- 学習対象にGitHub上のレポジトリがない場合  
  GitHub上に新しいレポジトリを作成  
  このレポジトリを学習フォルダ`learning`にクローン  
  `$ git clone 対象のURL`  
  新しく出来たフォルダをGitの作業フォルダにする  

## ローカルファイルのアップ
1. ローカルリポジトリのインデックスに新規もしくは修正したファイルをステージング    
`$ git add ファイル名`  
`$ git add -A`  
1. 新規もしくは修正をコミット  
`$ git commit -m "コメント"` 
-m: コメントオプション  
1. リモートレポジトリに変更を反映  
`$ git push origin master`  

  
