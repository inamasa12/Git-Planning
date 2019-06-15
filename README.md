# Git-Planning
Gitの利用方法を検討

## 検討 

### 現状のローカルフォルダ及びファイル管理方法
User/Anaconda3/PythonScripts内に学習単位毎のフォルダ  
基本、学習対象の書籍単位でフォルダが分かれている

### 新しい管理方法
User直下にGit管理のフォルダを作成（learning）
- 学習対象にGitHub上のレポジトリがある場合  
  当該レポジトリをフォーク（Fork）  
  フォークしたレポジトリをクローン（clone）して、当該フォルダをGitの作業フォルダにする
- 学習対象にGitHub上のレポジトリがない場合  
  GitHub上に新しいレポジトリを作成
  フォークしたレポジトリをクローン（clone）して、当該フォルダをGitの作業フォルダにする
