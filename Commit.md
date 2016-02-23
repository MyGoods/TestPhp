Windows 环境Github Shell 
=====

#### 前置条件:
 1. 到官网下载客户端：https://github-windows.s3.amazonaws.com/GitHubSetup.exe，完成安装，桌面有两个图标，Git Shell(命令行工具)和GitHub(图形界面)。
 2. 双击打开Git Shell

 
#### 操作步骤:
* 先输入*  pull origin master //先把远程服务器github上面的文件拉下来
* 再输入*  push origin master
* 如果出现报错 fatal: Couldn’t find remote ref master或者fatal: ‘origin’ does not appear to be a git repository以及fatal: Could not read from remote repository.
* 则需要重新输入*  remote add origingit@github.com:djqiang/gitdemo.git
  
  使用git在本地创建一个项目的过程
* makdir ~/hello-world //创建一个项目hello-world
* cd ~/hello-world //打开这个项目
* git init //初始化
* touch Commit.md
* add README //更新README文件,待提交
* commit -m 'add new file Commit.md' //提交更新，并注释信息“add new file”
* remote add origin git@github.com:defnngj/hello-world.git //连接远程github项目
* push origin master //将本地项目更新到github项目上去

######Other:
* $git config -l //查看配置路径，重点看remote.origin.url
* $git log -n l //已提交到代码仓库
* $git status //查看new file 待提交

 
#### 常见问题:
  1. 先输入$ ssh-agent，再输入$ ssh-add ~/.ssh/id_key，这样就可以了。
  2. 如果还是不行的话，输入ssh-add ~/.ssh/id_key 命令后出现报错Could not open a connection to your authentication agent.
     解决方法是key用Git Gui的ssh工具生成，这样生成的时候key就直接保存在ssh中了，不需要再ssh-add命令加入了，其它的user，token等配置都用命令行来做。
     最好检查一下在你复制id_rsa.pub文件的内容时有没有产生多余的空格或空行，有些编辑器会帮你添加这些的。
  3. 如果输入*  push origin master 提示出错信息：error:failed to push som refs to …….

  





