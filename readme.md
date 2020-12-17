# learn Git Note

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
