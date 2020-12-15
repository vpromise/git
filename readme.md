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
* 
