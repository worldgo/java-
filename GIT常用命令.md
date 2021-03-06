# GIT
>![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly93czEuc2luYWltZy5jbi9sYXJnZS8wMDZWckpBSmd5MWc1azB3enQwZ3ZqMzBtZDA2Zzc2dy5qcGc)  
## 工作中用到的git操作流程
1. 进入自己的工作代码文件夹
2. 右键git bash here 
3. git clone [远程url]
4. 进入克隆下来的文件夹 -克隆了整个仓库下来，包括仓库里面含有的分支等git信息；并且自动做了远程关联
5. 右键git bash here 
6. git checkout -b [本地分支名] [origin/远程分支名] -新建与远程分支同名的本地分支并关联；这种方式新建本地分支，分支初始化内容会是对应远程分支的内容，而不是本地master 
7. git pull origin [远程分支名] -拉取最新
## 目前常用命令
$git init  
\#初始化文件夹为git代码库目录

$git clone [url]  
\#直接克隆url项目到当前本地仓库，无需建立关联什么的

$git config --list  
\#查看上前的git配置，可以看用户名与email

$git config [--global] user.name "[name]"  
$git config [--global] user.email "[email]"
\#设置提交代码时的用户信息；email其实也是取个名，没太大用处

$git status  
\#查看当前工作区修改情况

$git add .  
\#添加工作区所有修改文件到暂存区  

$git commit -m '[message]'  
\#提交暂存区更新版本到历史记录区  

$git push  
\#推送更新版本到远程仓库  

**至此，一套大致目前用到的流程就走完了，但还有很多细节设置未写明  
实际操作  从本地新建git仓库到远程分支拉取推送版本 是最好的记忆方法**
---
## 新建分支
$git branch [name]  
\#新建本地分支

## 查看分支
$git branch  
\#查看本地分支 

$git branch -r  
\#查看远程分支  

$git branch -a  
\#查看本地和远程所有分支

$git remote -v  
\#可以查看已有的远程关联-这好比一条引线，线的两头可以绑在不同的分支

## 远程连接并提交
$git remote add [link-name] [remote-url]
\#添加关联 -**还未绑定分支**  
$git push --set-upstream [远程关联名] [本地分支名]  
>~~**远程对应分支是？**~~ - push后远程自动生成同名分支

$git remote remove [link-name]  
\#取消当前分支的远程关联

$git branch -vv  
\#查看现有的远程分支与本地分支的映射关联

## 切换分支
$git checkout -b [branch-name]  
\#新建分支并切换到该分支  

$git checkout [branch-name]
\#切换本地分支

## 删除分支
$git branch -d [name]  
\#删除本地分支

## 查看远程与本地仓库的不同
$git diff [local branch] [remote branch];   eg: $git diff master origin/master(remote/origin/master与origin/master效果相同    

## 拉取远程分支
$git fetch [关联名] ([远程分支名])  
\#同步远程仓库到本地仓库，并未更新到工作区 **当感觉状态不对劲时，可用作刷新**

$git checkout -b [本地分支名] [远程分支名]  
\#在本地新建分支并与远程分支关联 

$git pull (远程分支名)  
\#拉取远程分支内容到当前本地分支工作区与本地合并**？**--不会强制覆盖  

## 查看历史提交
$git log 
\#较详细展示

$git reflog  
\#简介展示  

## 拉取远程代码库。（本地分支与远程分支同名才能push）**？**
1. 新建文件夹后直接 $git clone [url]-克隆了整个仓库，不用初始化本地仓库。在进一层的文件夹中有.git文件，在这一层进去git bash
然后可以切换分支；$git log还可以查看历史提交记录 
2. 新建文件夹然后$git init ,$git pull [url] [远程分支名]-拉取了远程对应分支的最新代码；$git log还可以查看历史提交记录         
**push呢？**

## 小知识
>在clone之后，GIT会自动将远程仓库命名为origin(就是一别名)。查看分支时候以origin\开头的便是远程分支  

>local branch和remote branch是独立并行的，通过fetch和push进行交互  

>因为git的分支必须指向一个commit，没有任何commit就没有任何分支
>提交第一个commit后git自动创建master分支
>新建分支在commit之后才会被保存  
>键盘‘q’可以停止当前git命令运行


