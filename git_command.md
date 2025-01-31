◎ 新增帳號密碼：
git config --global user.name "xxx"
git config --global user.email "xxx.gmail.com"

◎ 將資料夾變為可以版本控制的儲存庫：
git init

◎ 檔案狀態：
git status
- 未追蹤(U) Ｕntracked
- 已追蹤(A) Tracked
- 已修改(M)
- 已暫存 Staged
- 已提交 Committed

◎ 將檔案變為已追蹤
git add 檔案名稱
git add *.md (所有副檔名為md的檔案)
git add . (所有檔案)

◎ 將檔案提交
git commit -m "給予的message"

◎ 檢視提交歷史
git log --oneline

◎ 檢視不同提交的差異
git diff 修改點id -- 檔案名稱

◎ 更改回某一版本
git checkout 修改點id -- 檔案名稱 (改到某一版本但保留後面的版本)
git reset -- hard 修改點id (改到某一版本並將後面的版本全刪除)

◎ 若是刪除檔案夾中的檔案，也須將該變化加入至“倉庫”中
（git追蹤的是檔案變化，而非檔案本身）

◎ 檔案不需要被追蹤時
- 在資料夾中建立 .gitignore
- 將需要忽略的檔名加入其中

◎ 新增協作者
- repositories setting -> collaborators ->新增成員email
◎ 協作者要做的事
- 將儲存庫pull到本地端：git clone https://......
- 有一方更新時，只需要使用 git pull 就可以將更新的內容拉到本地端
- 建立新分支：git checkout -b branch名稱
- push時要用分支名稱：git push origin branch名稱
❖ 在github頁面可發起pull request，請求將更改哪容加入主線分支

by https://www.youtube.com/watch?v=FKXRiAiQFiY


◎ 上傳相關指令
git remote add origin git@github.com:LWC13/git_test.git
git branch -M main
git push -u origin main

◎ 解決 git@github.com permission denied (publickey) fatal: Could not read from remote repository.
- 進入.ssh資料夾 cd ~/.ssh
- 產生鑰匙 ssh-keygen
- 複製.pub內容 cat ~/.ssh/id_rsa.pub
- 將密鑰貼至github Setting -> SSH and GPG keys -> New SSH key
- 重新push
by https://andytsai.coderbridge.io/2024/04/07/解決-git@githubcom-permission-denied-(publickey)/
