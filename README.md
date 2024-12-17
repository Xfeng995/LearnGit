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
# 3 远程仓库操作
## 3.1 查看远程仓库
显示远程仓库的地址。

git remote -v
## 3.2 添加远程仓库
添加一个新的远程仓库。

git remote add "remote-name" "repository-url"
## 3.3 推送到远程仓库
将本地分支推送到远程仓库

git push "remote-name" "branch-name"
## 3.4 拉取最新更改
拉取远程分支的最新更改并合并到当前分支。

git pull "remote-name" "branch-name"
## 3.5 获取远程分支
获取远程仓库的最新信息，但不会自动合并。

git fetch "remote-name"
# 撤销操作
## 4.1 撤销工作区更改
撤销对某个文件的修改，将其恢复到上次提交的状态。

git checkout -- "file"
## 4.2 撤销暂存区更改
将暂存区的文件撤回到工作区。

git reset HEAD "file"
## 4.3 撤销提交
撤销到指定提交，但保留更改在暂存区。

git reset --soft "commit-hash"

彻底撤销到指定提交，并删除所有更改。

git reset --hard "commit-hash"

# 5 标签管理
## 5.1 创建标签
为当前提交创建一个标签

git tag “tag-name”

创建带说明的标签

git tag -a "tag-name" -m "标签明说"

## 5.2 查看标签
列出所有标签

git tag
## 5.3 推送标签
将本地标签推送到远程仓库

git push "remote-name" "tag-name"
## 5.4 删除标签

git tag -d "tag-name"

删除远程标签

git push "remote-name" --delete "tag-name"

# 6使用技巧
## 6.1 忽略文件
在项目根目录创建 .gitignore 文件，列出需要忽略的文件或文件夹：

忽略所有 .log 文件

*.log

忽略 tmp 文件夹及其内容

/tmp
## 6.2 配置别名
为常用命令配置别名：使用 git st 代替 git status。

git config --global alias.st status

git config --global alias.co checkout

git config --global alias.br branch
## 6.3 查看配置
显示当前 Git 配置。

git config --list
# 7. 常见问题解决
## 问题 1：合并冲突
合并时可能出现冲突，需要手动解决：

打开冲突文件，按照标记（<<<<<<<、=======、>>>>>>>）解决冲突。添加修改后的文件到暂存区：

git add "file"

提交合并：

git commit
## 问题 2：恢复误删的分支
如果不小心删除了分支，可以用以下方法恢复：

git reflog

git checkout -b "branch-name" "commit-hash"
## 问题 3：回滚远程提交
如果误推了错误的提交，可以使用：

git revert "commit-hash"

git push

# 8 总结
xx总结
