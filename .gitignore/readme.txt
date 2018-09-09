nosql===>redis+mysql
键 值
string---》字符串，int
hash---->字典
list----》列表
set-----》集合
zset----》有序集合
====================版本控制系统
作用：更方便的管理源代码
对于个人：后悔药
对于团队：合并
====================git简介
分布式：将数据存储在多台电脑上
版本控制：
====================单人本地操作
git init--->将磁盘目录变成仓库，会在目录下新建隐藏目录.git
git status--->查看工作区，是否有内容需要提交
git add .===>将当前目录的内容由工作区加入到暂存区
git commit -m '说明信息'---->将暂存区的内容提交到仓库区
git log或git reflog====>查看历史版本信息
git reset 版本号====》将仓库区的指定版本恢复到暂存区
git checkout -- 文件名====>将暂存区指定的文件恢复到工作区
====================多人远程操作
命令：与服务器交互的命令
------创建远程仓库
1.https://gitee.com/，注册账号
2.新建仓库
3.创建忽略文件.gitignore
	*.pyc
	.idea/
------配置SSH
1.sudo rm -rf .ssh
2.ssh-keygen -t rsa -C "注册gitee时的邮箱"
3.三次回车
4.cd .ssh
5.cat id_rsa.pub
6.复制公钥，到gitee中进行添加
------克隆项目
git clone 地址
------多人协同开发
git push origin master===>某个员工将本地文件，提交到服务器
git pull====>从服务器获取代码
------代码冲突
当多个员工，修改同一个文件时，会产生冲突
协商
------标签
阶段性的标记
------分支
每个员工在不同的分支上写代码，互不影响
公用分支：
	dev--->开发的阶段性合并
	master-->在dev分支的代码，经测试无bug后，由经理合并过来，再由运维进行布署
git branch===>查看所有分支
git branch 名称===》新建分支
git checkout 名称===》切换分支
git merge 分支名称===》将指定分支的代码，合并到当前分支
====================总结
1.注册gitee.com账号
2.新建仓库
3.新建.gitignore文件
	*.pyc
	.idea/
4.新建分支dev
5.配置ssh公钥
6.克隆git clone ****
7.根据服务器创建dev分支
	git checkout -b dev origin/dev
8.新建自己的分支
	git checkout -b itcast
9.在仓库目录下，新建项目，如xjzx
10.复制资源到项目中
11.使用最多的命令：
	git add .
	git commit -m ''
	git push origin itcast
https://www.yuntongxun.com/===>免费发送短信
https://www.qiniu.com/========>免费的文件存储服务器