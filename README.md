# GIT 基础操作
## 1.1 初始化仓库
在当前目录初始化一个新的 Git 仓库。

git init

本地会生成一个.git的隐藏文件
## 1.2 克隆远程仓库
将远程仓库克隆到本地。

git clone "repository-url"
## 1.3 查看状态
查看工作目录中文件的状态（修改、未跟踪、暂存等）。

git status
## 1.4 添加文件到暂存区
将指定文件添加到暂存区。

git add "filename"

将当前目录下的所有文件添加到暂存区。
git add .
## 1.5 提交更改
将暂存区的更改提交到本地仓库。

git commit -m "描述提交的更改"
## 1.6 查看提交记录
显示提交历史

git log

以简洁形式显示提交历史。

git log --oneline
## 1.7 查看差异
查看工作区与暂存区之间的差异。

git diff

比较两个分支之间的差异。

git diff "branch1" "branch2"

# 2 分支管理
## 2.1 创建分支
创建一个新的分支

git branch "branch-name"
## 2.2 切换分支
切换到指定的分支

git checkout "branch-name"

## 2.3 创建并切换分支
创建一个新分支并切换到该分支。

git checkout -b "branch-name"

## 2.4 合并分支
将指定分支合并到当前分支。

git merge "branch-name"
## 2.5 删除分支
删除本地分支（如果该分支未完全合并到当前分支，会提示错误）。

git branch -d "branch-name"

强制删除分支。

git branch -D "branch-name"