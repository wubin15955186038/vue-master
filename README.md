# vue2-master

## git常用命令集合：

    git init

    创建版本库 (生成例：/.git/目录)

    以下命令都需要拥有版本库的时候才可以执行

    git add <file>

    用于把文件添加到git（暂存区），准备提交【请忽略<>】

    git add -A  或者 git add -all

    把工作区的所有修改添加到暂存区

    git commit -m '描述内容'

    只有添加文件之后才能使用，用于提交内容到主分支（默认是master）

## 本地其它命令合集：

    git status

    查看仓库状态

    git diff

    查看修改的内容。注意：已经使用git add之后，不能再查看修改的内容

    git log

    查看git提交日志 记录git commit信息

    git reflog

    记录每一次git的命令（该命令可用于回滚后忘记最新版的id是找回）

    HEAD 在git中指代当前版本 HEAD^指上一个，HEAD^^同理

    git checkout -- <file>

    撤销文件的修改到最近一次git commit或者git add 注意：--非常重要 【请忽略<>】

    git reset --hard <commit_id>

    把工作区内容恢复到指定版本 【请忽略<>】

    git reset HEAD <file>

    把暂存区的内容清除 【请忽略<>】

    git rm <file>

    删除文件。删除之后还需要提交（git commit）【请忽略<>】

    git mv <filedir> <newfiledir>

    移动文件到新的路径，如果新的文件名发生改变，则可以理解为重命名【请忽略<>】

    例子：git mv 12.txt 45.txt

    把当前目录下的文件12.txt重命名为45.txt

    git mv 45.txt ./dir/67.txt

    把当前目录下的文件45.txt移动到当前目录下的dir目录中，并重命名为67.txt

## 远程仓库命令合集：

    git remote add origin <address>

    关联一个github远程仓库 <address>是仓库地址 【请忽略<>】

    git push -u origin master

    关联远程仓库第一次提交的时候添加上-u参数，用于把本地以前的commit_log推送到远程库

    git push origin master

    以后的推送就不需要-u参数

    git remote rm origin

    移除远程库

    git remote add origin "Git仓库的ssh格式地址"

    添加远程库

    git clone <adderss>

    克隆一个已有的远程仓库。address是远程库地址【请忽略<>】

## 分支管理命令合集：

    git checkout -b <newbranch>

    创建一个新的分支并切换到这个新的分支。-b参数表示创建新分支 newbranch 新的分支名【请忽略<>】

    git branch <newbranch>

    创建一个新的分支，newbranch 新的分支名【请忽略<>】

    git checkout <branch>

    切换到指定分支【请忽略<>】

    git branch

    查看当前仓库拥有的分支，以及当前在哪一个分支（分支名前有*表示当前所在分支）

    git merge <branch>

    合并指定分支的更新到当前所在分支【请忽略<>】

    git branch -d <branch>

    删除指定分支【请忽略<>】

    git branch -D <branch>

    强制删除指定分支【请忽略<>】

## 其它命令集合：

    git log --graph

    显示分支合并图

    git merge --no-ff <branch>

    关闭Fast-forward 合并（快速模式），强制禁用快速合并模式进行合并指定分支到当前分支【请忽略<>】

    git stash

    保存当前分支工作现场，可以执行多次

    git stash list

    查看当前分支保存的工作现场列表

    git stash apply [stash_id]

    恢复现场，方括号内是可选参数（指定恢复）【请忽略[]】

    git stash pop [stash_id]

    恢复现场，并删除【请忽略[]】

    git stash drop [stash_id]

    删除现场【请忽略[]】

    git remote

    查看远程库信息，默认显示origin

    git remote -v

    查看更详细的远程库信息，包括push 和fetch 地址

## 本文描述的命令还不是很全面，更详细的请运行

    git --help

查阅
