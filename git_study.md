1、命令窗口（Command Prompt）或 PowerShell

命令：
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
$ git config list
$ git config uer.name

git help <verb>
$ git <verb> --help
$ man git-<verb>
git help config
$ git clone https://github.com/libgit2/libgit2 mylibgit
http://git-scm.com/book/zh/v2/%E5%85%B6%E5%AE%83%E7%8E%AF%E5%A2%83%E4%B8%AD%E7%9A%84-Git-%E5%9B%BE%E5%BD%A2%E7%95%8C%E9%9D%A2


1,从已有的分支创建新的分支(如从master分支),创建一个dev分支

git checkout -b dev

2,创建完可以查看一下,分支已经切换到dev

git branch

    * dev

    master

3,提交该分支到远程仓库

git push origin dev

4,测试从远程获取dev

git pull origin dev

或者：

如果用命令行，运行 git fetch，可以将远程分支信息获取到本地，再运行 git checkout -b local-branchname origin/remote_branchname  就可以将远程分支映射到本地命名为local-branchname  的一分支

5,我觉得现在重要的就是设置git push,pull默认的提交获取分支,这样就很方便的使用git push 提交信息或git pull获取信息

git branch --set-upstream-to=origin/dev

取消对master的跟踪

git branch --unset-upstream master

6,现在随便修改一下工程文件的内容,然后git commit ,git push,之后就可以直接提交到远程的dev分支中,而不会是master




m：
git clone http://gitlab.bailitop.com/dongxuepeng/test.git mengbaoqing


cd mengbaoqing

git config user.user "mengbaoqing"
git config user.email "1129514277@qq.com"
git branch mengbaoqing
git checkout mengbaoqing
ls
touch mengbaoqing.txt
git add mengbaoqing.txt
git commit -m "1"
git push origin mengbaoqing


d：
git branch dev
git pull origin dev
git branch mengbaoqing
git checkout mengbaoqing
git pull origin mengbaoqing
git checkout dev
git merge orinig mengbaoqing
git checkout master
ls
==============================================================================
个人开发环境：
	个人1
	个人2
	个人3
	个人N


开发环境： Development
	master
	test 测试分支
	PRO 产品分支（生产分支）


生产环境 Production

主分支 master
开发分支 develop 
功能分支 feature 
预发布分支  release
bug 分支 fixbug
其它分支 other


暂存区：
git stash or git stash pop

http://www.topthink.com/topic/727.html?utm_source=tuicool
http://gitlab.bailitop.com/dongxuepeng/test/tree/master
http://www.360doc.com/content/14/0508/17/14416931_375851686.shtml
函数库：https://www.kernel.org/pub/software/scm/git/docs/
克隆远程仓库：git clone https://github.com/wenziyelang/curl_baidu.git
增加一个文件：git add test.txt
提交一个文件：git commit -m "这是注释"
查看状态：git status
编辑文件：vim test.txt
查看文件内容：cat test.txt
上传本地当前分支代码到master分支  git push origin master
上传本地所有分支代码到远程对应的分支 git push
合并分支：git merge mengbaoqing
查看分支 git branch -a
创建分支 git branch name
切换分支 git checkout name
创建并切换 git checkout -b name
合并某分支到当前分支 git merge name
删除分支 git branch -d name
提交该分支到远程仓库 git push origin dev
测试从远程获取dev  git pull origin dev
不用add直接commit  ： git commit -a -m 'added new benchmarks'
删除一个文件：git rm PROJECTS.md
文件改名： git mv file_from file_to

查看一下分支合并日志：git log --graph --pretty=oneline --abbrev-commit 
回到过去版本：	git reset --hard master@{1}
修改了，没有git add，已提交过 想撤销这次修改，git checkout a.txt or /src/
修改了，已git add，git reset a.txt
撤销到某一个版本，但是当前暂存区、工作区不想撤销，git reset --soft commitId
如果修改了某几个文件到暂存区，想撤销到某个commit，git reset --hard commitId
git can-file -p HEAD

git stash 
git stash pop


