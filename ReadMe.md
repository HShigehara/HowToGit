#[基本的な流れ]
1. `git init <dir_name>` #リポジトリの作成
2. `git add <file1> <file2>`  #ステージングエリアにファイルを追加
3. `git commit -m "commit message"` #更新内容を記述してファイルをコミット
4. 2,3の繰り返し

#[リモートにも反映させたいなら]
1. `git init` #リポジトリを作成したいディレクトリ内でリポジトリを作成(又は"`git clone https://git/remote/pass/repo.git"`でフォルダごと作る)
2. `git remote add origin https://git/remote/pass/repo.git`
3. `git add <file1> <file2> ...` #ファイルの追加("."とすればカレントディレクトリの全てのファイルを追加できる)
4. `git commit -m "commit message"` #変更点などのメッセージを記述
5. `git push -u origin master` #リモートにプッシュ

#[…or create a new repository on the command line]
`echo # test >> README.md`
`git init`
`git add README.md`
`git commit -m "first commit"`
`git remote add origin https://git/pass/repo.git` #リモートに追加
`git push -u origin master` #リモートにプッシュ

#[…or push an existing repository from the command line]
`git remote add origin https://git/pass/repo.git`
`git push -u origin master`

#[その他]
`git status` #現在のステータス確認
`git log` #更新履歴の確認
`git checkout <commit_id>` #あるリビジョンに戻る
`git checkout master` #masterブランチの最新版に戻る
`git checkout <commit_id> <filename>` #特定のファイルだけあるリビジョンのものと同じ状態にする