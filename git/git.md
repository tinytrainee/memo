# Git Knowledge

# Basic
## Link to local folder
- フォルダでコマンドプロンプト実行
- `git clone <URL> [フォルダ名]`
  - フォルダ名を指定しない場合, リモート側での名前でフォルダが作成される

## Reflect local changes
- 変更対象をステージへ追加
  - git管理されていないファイル等をgit管理対象とするのがステージ
  - `git add [オプション] [ファイル名]`
  - オプション
    - `-A`
      - すべてのファイルをステージする
- ステージされたファイルに対する変更にローカル内でバージョンを付ける
  - `git commit [オプション] [ファイル名]`
  - オプション
    - `-a`
      - すべての変更をコミットする
    - `-m` 
      - コメントを付けてコミットする
- リモートへプッシュ
  - `git push --set-upstream リモート名 ブランチ名`


## Get Remote and Branch name
`git branch -a`