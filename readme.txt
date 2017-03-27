切换目录
$ cd 目录

创建仓库
$ mkdir 仓库名字

显示当前目录
$ pwd

初始化一个Git仓库，
$ git init

添加文件到Git仓库，分两步：

第一步，使用命令git add <file>，注意，可反复多次使用，添加多个文件；

第二步，使用命令git commit -m "注释"，完成。

仓库当前的状态
$ git status

比较差异
$ git diff readme.txt

历史记录 如果嫌输出信息太多，看得眼花缭乱的，可以试试加上--pretty=oneline参数：
$ git log --pretty=oneline
分支合并图
git log --graph --pretty=oneline --abbrev-commit

版本回滚 上一个版本就是HEAD^，上上一个版本就是HEAD^^，HEAD~100。
$ git reset --hard HEAD^
回退最新版本
$ git reset HEAD readme.txt

查看文件内容
$ cat readme.txt

查看命令历史
$ git reflog

删除文件，等同文件夹直接删除
$ rm 文件名

版本库中删除该文件
$ git rm 文件名
rm '文件名'
$ git commit -m "remove 文件名"

版本库里的版本替换工作区的版本
$ git checkout -- test.txt

github远程仓库连接
$ git remote add origin git@github.com:13236605001/JinHu.git
本地仓库同步远程仓库, -u 本地的master分支和远程的master分支关联
$ git push -u origin master
$ git push origin master

从githun上面clone到本地
$ git clone git@github.com:13236605001/JinHu.git

创建分支
$ git checkout -b zn   或   $ git branch zn
指向分支
$ git checkout zn

查看分支
$ git branch

合并某分支到当前分支,--no-ff，禁用“Fast forward”合并模式
$ git merge --no-ff -m "注释内容" zn

删除分支
$ git branch -d zn
强行删除分支
$ git branch -D <name>

把当前工作现场“储藏”起来
$ git stash
恢复工作现场，stash内容并不删除
$ git stash apply
删除stash内容
$ git stash drop
恢复工作现场并删除stash内容
$ git stash pop
查看工作现场
$ git stash list

查看远程库，-v 显示更详细信息
$ git remote -v