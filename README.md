# Learning-notes
深度学习、Linux、ROS、OpenCV、PCL、数学、编程等学习笔记。


# 1、安装
$ apt-get install libcurl4-gnutls-dev libexpat1-dev gettext libz-dev libssl-dev
$ apt-get install git
$ git --version
git version 1.8.1.2

# 2、配置
	/etc/gitconfig 文件：系统中对所有用户都普遍适用的配置。若使用 git config 时用 --system 选项，读写的就是这个文件。
	~/.gitconfig 文件：用户目录下的配置文件只适用于该用户。若使用 git config 时用 --global 选项，读写的就是这个文件。
	当前项目的 Git 目录中的配置文件（也就是工作目录中的 .git/config 文件）：这里的配置仅仅针对当前项目有效。每一个级别的配置都会覆盖上层的相同配置，所以 .git/config 里的配置会覆盖 /etc/gitconfig 中的同名变量。

用户信息
配置个人的用户名称和电子邮件地址：
$ git config --global user.name "runoob"
$ git config --global user.email test@runoob.com

查看配置信息
$ git config --list

编辑配置信息
$ git config -e

# 3、创建仓库 git init newrepo
$ git init Learning-notes

# 4、克隆 git clone <repo> <directory>
$ git clone https://github.com/zhengmaoch/Learning-notes.git

# 5、提交文件到本地仓库
$ git status -s
$ git add *.c
$ git add README
$ git commit -m '初始化项目版本'

# 6、上传远程代码并合并git push <远程主机名> <本地分支名>:<远程分支名>
$ git push origin master

# 7、删除文件
$ git rm hello.php 

# 8、移动或重命名
$ git mv README README.md

# 9、下载远程代码并合并git pull <远程主机名> <远程分支名>:<本地分支名>
$ git pull origin master