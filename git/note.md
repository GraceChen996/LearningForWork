# 概述

## 版本控制方式

1. 集中式版本控制工具

   版本库集中存放在中央服务器，用户从中央服务器下载代码，个人修改后提交到中央版本库，所以必须要联网才能工作。

   例子：SVN和CVS

2. 分布式版本控制工具

   没有”中央服务器“，每个人的电脑上都是一个完整的版本库，工作时无需联网，多人协作只需要将各自的修改推送给对方，就能互相看到对方的修改了

   例子：Git

## Git工作流程图

![image](image\image-20231117181532442.png)



# 常用命令

## 获取本地仓库

1. 在电脑上创建一个空目录作为本地Git仓库

2. 进入该目录，git bash here

3. 执行命令

   ```
   git init
   ```

   初始化如果成功，就能在文件夹下看到一个.git目录



## 基础操作指令

![image](image\image-20231117182943591.png)

 

1. 对文件进行修改或者创建文件以后，用git add命令让文件进入暂存区。通过.gitignore文件可以设置在add .时不移入暂存区的文件

   ```
   git add file1.txt //将某个文件的修改移入暂存区
   git add . //将所有修改都移入暂存区
   ```

   

2. 用git commit 命令提交修改

   ```
   git commit -m "add file1,fil2,xxx" //-m 后面的内容是提交的描述信息
   ```

   

3. 用git log查看提交记录

   ```
   git log[options]
   options
   	--all 显示所有分支
   	--pretty=oneline 将提交信息显示为一行
   	--abbrev-commit 使输出的commitid更加简短
   	--graph 以图的形式显示
   ```

   可以用alias指令给长指令设置别名，避免每次都要输入很长的指令



## 版本回退

1. 通过git log显示版本提交记录

2. git reset --hard commitid

   注意：自己用的时候可以这么用，和别人一起合作的时候最好不要这么回退

3. git reflog能够记录所有的操作，如果不慎reset了，可以用reflog查找回退之前的记录来撤销回退



