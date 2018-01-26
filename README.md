# Git学习

git在平时工作学习中都会用到，但是平时经常用到的只是非常少的几个命令，有时候遇到问题可能两个简单的命令就能解决，但是自己却经常大费周折，走了不少弯路，所以感觉有必要进行Git进阶学习。

## Git常用命令

这里根据Git命令的用途进行分类。

### 分支相关命令

1. 基于远程的master分支创建新的分支：`git checkout -b <newBranchName> origin/master`
2. 删除本地分支：`git branch -D <branchName>`
3. 删除远程分支：`git push origin :<branchName>`
4. 修改本地分支名称：`git branch -m <originName> <newName>`
5. 查看分支：`git branch` `-r`代表远程分支，`-a`代表全部分支

### 撤销操作相关命令

1. 取消工作区的修改
  - 单个文件：`git checkout — <fileName>`
  - 全部文件：`git checkout .`
2. 修改最后一次提交：`git commit —-amend -m`
3. 回到上次提交的版本：`git reset —-soft HEAD^`、`git reset —-hard HEAD^`
4. push后回到上个版本：`git revert HEAD^`

### stash命令

1. 储藏当前工作：`git stash`
2. 查看stash：`git stash list`, `git stash show -p stash@{0}`