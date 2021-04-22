# git_tutorial
## 確認したい操作一覧
参考文献: https://book.git-scm.com/
- gitコマンドでは、--helpオプションをつけると、指定したコマンドの詳細情報を把握できる
- git switch
    - -cでブランチを新規作成して、checkoutする
- git restore
    - 指定したファイルなどの変更をなくす
- [git rebase](https://git-scm.com/book/ja/v2/Git-%E3%81%AE%E3%83%96%E3%83%A9%E3%83%B3%E3%83%81%E6%A9%9F%E8%83%BD-%E3%83%AA%E3%83%99%E3%83%BC%E3%82%B9)
    - --onto,
    - --continue,
    - --abort,
    - -i
        - fixup: 指定したcommitメッセージを削除し、前のcommitと融合する
        - squash: 前のコミットと融合し、コミットメッセージを編集できる
    - git pull --rebase
- git commit
    - インデックスの状態を記録する(addは、変更をインデックスに登録する)
    - --allow-empty
    - [--amend](https://book.git-scm.com/book/en/v2/Git-Basics-Undoing-Things): 前のcommitの修正を行う
- git revert
    - rebert...元に戻す
    - 取り消したいこっ水戸を打ち消すようなコミットを新しく作成する
    - revertしたことがバージョン管理されるため、リモートにpushされて公開されているcommitに対しても安全に使えるらしい
    - メッセージの編集: -e or --edit(default)、編集しない: --no-edit
    - コミットしない: -n...indexに戻すだけでcommitまで行われないようにする
    - マージコミットの取り消しにおける、マージした2つのコミット(親)のうちどちらに戻すのかを指定する(オプションなしではできない): -m parent-number
    - ex) git revert HEAD~3, git revert -n master~5..master~2
- git tag
- git rm
- cherry-pick
- github actions
- ssh接続