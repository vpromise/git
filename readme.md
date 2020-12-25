# Learn Git Note

This file is my note for git learning.

## Basic Usage

1. `git init`
2. `git add <file>`
3. `git commit -m <message>`

   ```python
   git add readme.md
   git commit -m "new readme.md files"
   ```

* 查看状态 `git status`
* 查看不同 `git diff`
* 查看日志 `git log` or `git log --pretty=oneline`
* 查看历史 `git reflog` 查看命令历史，以便确定要回到未来的哪个版本
* 版本回退 `git reset -hard HEAD^` or `git reset -hard <commit id>`
  - 参数： `HEAD^` `HEAD^^` `HEAD~100`
* `git checkout -- file` 丢弃工作区的修改
* `git reset HEAD <file>` 撤销暂存区的修改，重新放回工作区
* 删除文件 `git rm <files>`

## Remote Repository

* 创建SSH Key `ssh-keygen -t rsa -C "youremail@example.com"`
* 注册 GitHub,添加 SSH Pub Key
* GitHub 新建 Repository *learngit*
* 关联远程Repository `git remote add origin git@github.com:username/learngit.git`
* 推送 `git push -u origin master`
* `git clone`

## Branch

### New Branch and Merge

* 创建`dev`分支并切换到`dev`分支: `git checkout -b dev`
* 等价于

  ```
  git branch dev
  git checkout dev
  ```
* `git checkout master`
* `git merge dev`
* 删除dev分支：`git branch -d dev`
* 查看分支 `git branch`
* 创建分支 `git branch <name>`
* 切换分支 `git checkout <name>`或者`git switch <name>`
* 创建+切换分支 `git checkout -b <name>`或者`git switch -c <name>`
* 合并某分支到当前分支 `git merge <name>`
* 删除分支 `git branch -d <name>`
* `git merge --no-ff -m "merge with no-ff" dev`
* `git stash` “储藏”当前工作现场,`git stash list` 查看
* `git stash apply` 恢复，但stash内容并不删除，需要用 `git stash drop` 来删除
* 或者用 `git stash pop`，恢复的同时把stash内容也删除了
* `cherry-pick` 复制一个特定的提交到当前分支
* 通过 `git branch -D <name>` 强行删除没有被合并过的分支
* 查看远程库信息 `git remote -v`
* 本地推送分支，使用 `git push origin branch-name`，如果推送失败，先用 `git pull` 抓取远程的新提交
* 在本地创建和远程分支对应的分支，使用 `git checkout -b branch-name origin/branch-name`，本地和远程分支的名称最好一致
* 建立本地分支和远程分支的关联，使用 `git branch --set-upstream branch-name origin/branch-name`
* 从远程抓取分支，使用 `git pull`，如果有冲突，要先处理冲突
* `git rebase` 提交记录变成一条直线

## Tag

* `git tag <name>` 就可以打一个新标签
* `git tag` 查看所有标签