# Git-Planning
Gitの利用方法

## 学習環境の設定
インストール後、user.nameとuser.emailを登録  
`git config --global user.name "～"` and `git config --global user.email ～`

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
- Git  
  [GitのHEADとは何者なのか](https://qiita.com/ymzk-jp/items/00ff664da60c37458aaa)
- Markdown記法全般  
  [Markdown記法 サンプル集](https://qiita.com/tbpgr/items/989c6badefff69377da7)  
  [Markdown記法 チートシート](https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa)  
- 数式  
  [GithubのREADMEとかwikiで数式を書く](http://idken.net/posts/2017-02-28-math_github/)  
  [よく忘れるので数学のTeX記法をまとめ](https://qiita.com/shepabashi/items/27b7284d1f0007af533b)  
  [LaTeXコマンド集](http://www.latex-cmd.com/)  
- 画像  
  [GitHubに画像ファイルを保存してREADME.mdで表示する方法](https://www.pupha.net/archives/1632/)  

# その他
## コマンドライン（Windows）
テキストエディタの起動:  
  `$ notepad ファイル名`  
ファイル内容の表示:  
  `$ type ファイル名`
