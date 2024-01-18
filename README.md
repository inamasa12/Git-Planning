# Git-Planning  

## Git操作

- フォーク  
異なるアカウントのレポジトリをコピーする

- クローン  
リモートレポジトリをローカルにコピーする  
`git clone repo_A(SSH)`: リモートレポジトリrepo_Aをローカルに取得  

- アド
変更をステージングエリアに登録する  

- コミット  
変更を確定させる  

- プッシュ  
ローカルブランチをリモートにコピーする  
`git push origin branch_A`: ローカルのbranch_Aブランチをリモートレポジトリoriginにコピー  

- プルリクエスト  
ブランチのマージを目的に変更のレビューを依頼する  

- マージ  
異なるブランチを同期する  
異なるブランチで行った変更を目的のブランチに反映させる

- フェッチ  
リモートブランチの状態を記録する「リモート追跡ブランチ」を最新の状態に更新する  
全てのブランチが対象  
`git fetch origin`: リモートレポジトリoriginに関する全てのリモート追跡ブランチを更新  

- プル  
フェッチとマージを続けて行い、ローカルブランチをリモートブランチと同じ状態にする  
`git pull origin master`: ローカルのmasterブランチをリモートレポジトリoriginのmasterブランチに同期（処理の前に更新対象のブランチに移動しておく必要がある）  

- プルリクエスト  
変更のレビューを依頼すること  


---
## Gitコマンド
- git init  
ローカルレポジトリを作る

- git status  
ファイルの更新状態を確認  
- git diff  
ファイルとステージングエリアの差分を確認  
- git diff --cached  
ステージングエリアと前回コミットの差分を確認  
- git diff branch_A  
作業ブランチとbranch_Aの差分を表示  
- git log (-p)  
コミット履歴を確認  
pオプションで各コミットの差分も表示  
- git remote -v  
リモートレポジトリの設定を確認  

- git branch  
作業ブランチを確認  
- git branch branch_A  
branch_Aを作成  
- git branch -d branch_A  
ローカルのbranch_Aを削除  

- git checkout branch_A (git switch)  
作業ブランチをbranch_Aに移動  
当該ブランチがリモート追跡ブランチにあって作業ブランチにない場合は、リモートのブランチがコピーされる  
- git checkout -b branch_A  
ブランチの作成と当該ブランチへの移動を同時に行う  
- git checkout -- file_A (git restore)  
file_Aへのコミットを取り消す  
本来的にはfile_Aをステージングの状態に戻す操作  
- git reset HEAD file_A (git restore)  
ステージングエリアへの登録を取り消す  
本来的にはステージングエリアを最新のコミットの状態に戻す  

- git add file_A  
file_Aの変更をステージングエリアに登録  
- git add -A  
レポジトリ内の変更をまとめてステージングエリアに登録  
- git commit -m "COMMENT"  
ステージングエリアの登録をコミット  
- git commit -am "COMMENT"  
ステージングとコミットを連続して行う  

- git push origin branch_A  
ローカルブランチbranch_Aの変更をリモートに反映させる  

- git rm file_A  
file_Aファイルを削除して、変更をステージングエリアに登録（コミットはしない）  
- git rm -r dir_A  
dir_Aディレクトリを削除して、変更をステージングエリアに登録（コミットはしない）  

- git merge branch_A  
カレントのブランチにbranch_Aの状態を反映させる  


---
## Gitの大まかな流れ  
リモートはGitHubを前提  
1. ローカルレポジトリの作成  
    1. 既存のプロジェクト（レポジトリ）が存在する  
    ① GitHub上で対象のプロジェクトをフォーク  
    ② フォークしたレポジトリをローカルにクローン  
    　　`git clone repo_A(SSH)`  
    1. 新しくプロジェクトを立ち上げる  
    ① GitHub上にレポジトリを作成  
    ② ローカルにレポジトリと同名のフォルダを作成（デフォルトのブランチ名はmasterを前提としているので注意）  
    ③ 当該フォルダでレポジトリを設定  
    　　`git init`  
    ④ リモートレポジトリを紐づけ  
    　　`git remote add origin repo_A(SSH)`  
    ⑤ ローカルをリモートに同期  
    　　`git pull origin master`  
1. ローカルでのファイル変更  
1. 変更のステージング  
　`git add file_A`
1. 変更のコミット  
　`git commit -m "COMMENT"`
1. 変更のプッシュ  
　`git push origin master`


---
## 用語  
- master (main)  
レポジトリで最初に自動作成されるブランチ  
- origin  
コピー（クローン）元のリモートレポジトリ  
- HEAD  
作業対象ブランチの最新のコミットへのポインタ  
- 3種類のマージ  
マージコミット: トピックブランチのコミットを全て維持する  
スカッシュ: トピックブランチのコミットはまとめる    
リベース: 全てのコミットを直列させる  
## 参考サイト
- Markdown記法全般  
  [Markdown記法 サンプル集](https://qiita.com/tbpgr/items/989c6badefff69377da7)  
  [Markdown記法 チートシート](https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa)  
- 数式  
  [GithubのREADMEとかwikiで数式を書く](http://idken.net/posts/2017-02-28-math_github/)  
  [よく忘れるので数学のTeX記法をまとめ](https://qiita.com/shepabashi/items/27b7284d1f0007af533b)  
  [LaTeXコマンド集](http://www.latex-cmd.com/)  
- 画像  
  [GitHubに画像ファイルを保存してREADME.mdで表示する方法](https://www.pupha.net/archives/1632/)  
  [GitHub/README.md に画像を表示させる簡単な方法](https://qiita.com/ROY_M/items/2c4feb5de05535441bc8)  
  [GitHubの画像貼り付けでサイズを指定する方法](https://dackdive.hateblo.jp/entry/2015/05/08/110029)  

<img src="https://user-images.githubusercontent.com/51372161/129022763-34be4463-dc02-4542-95df-57601609d4dc.png" width="320px">

