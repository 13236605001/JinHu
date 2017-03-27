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