# 基本流程

##### 一、基础配置与初始化

###### 1.配置用户信息

 	git config --global user.name "你的名字"

 	git config --global user.email "你的邮箱"

###### 2.初始化与克隆

 	git init	在当前目录建立一个新的Git仓库

 	git clone \[URL]	下载远程项目到本地

##### 二、暂存与提交

###### 1.检查状态

 	git status	查看哪些档案被修改、哪些已进入暂存区

###### 2.加入暂存区

 	git add \[file]		将特定档案加入暂存

 	git add .		将所有修改过的档案加入暂存

###### 3.提交变更

 	git commit -m "描述讯息"		将暂存区的内容正式记录到仓库中

 	git commit --amend		修改上一次的提交

##### 三、分支管理

###### 1.查看与建立

 	git branch	列出所有本地分支

 	git branch \[name]	创建新分支

###### 2.切换分支

 	git checkout \[name]		切换到该分支

 	git checkout -b \[name] <ref>		在ref上创建并立即切换到新分支，如果不写ref，默认在当前HEAD上创建

###### 3.合并与删除

 	git merge \[name]		将指定分支合并到当前分支

 	git branch -d \[name]		删除已合并的分支

##### 四、远程同步

###### 1.更新与下载

 	git pull		从远程下载更新并直接合并

 	git fetch		从远程下载更新，但不自动合并

###### 2.上传

 	git push origin \[branch\_name]		将本地分支推送到远程仓库

##### 五、撤回与回滚

###### 1.撤销暂存

 	git restore --staged \[file]		将文件移除暂存区，保留修改

###### 2.重置版本

 	git reset --hard HEAD^	强制回到上一个版本

 	git reset --hard HEAD~\[n]		回退到n个版本

 	git log		查看详细提交记录

# 其他

###### 关于文件操作

 	git diff \[file]	查看文件修改了哪些内容

 	git reflog	查看历史记录的版本号id

 	git checkout -- \[file]	把文件在工作区的修改全部撤销

 	git rm \[file]	删除文件

###### 关于隐藏与恢复

 	git stash	把当前的工作隐藏起来，等以后恢复现场后继续工作

 	git stash list	查看所有被隐藏的文件列表

 	git stash apply		恢复被隐藏的文件，但是内容不删除

 	git stash drop	删除文件

 	git stash pop	恢复文件的同时也删除文件

###### 关于远程库

 	git remote add origin \[URL]	关联一个远程库

 	git remote	查看远程库的信息

 	git remote -v	查看远程库的详细信息

###### 关于移动记录

 	git rebase <ref1> <ref2>		将当ref2移到ref1上(<ref>指的是任何能被Git识别成提交记录的引用)

 	git rebase -i <ref>~n		将HEAD前n个记录进行交互式rebase

###### 关于移动分支

&nbsp;	git branch -f \[name1] \[name2]		将name1分支移动到name2分支对应的记录上

###### 关于reset和revert

 	git reset对远程分支无效，为了撤销更改并分享给别人，需要用git revert

###### 关于cherry-pick

 	git cherry-pick <ref> <ref> <ref>	将多个记录按顺序抓取到当前分支上

###### 关于标签tag

 	git tag \[name\_tag] <ref>	给指定记录打上标签

 	git describe <ref>	查看离<ref>最近的标签,输出格式为<tag>-<numCommits>-g<hash>,当ref上有标签时，只输出标签名称







朋友————————————————>习惯了一个人的存在———————————>喜欢

和一个人可以很好的相处，无所谓得失——>和一个人可以很好的相处，但是害怕失去——>和一个人可以很好的相处，害怕失去，同时相处得很开心

比如说无所谓他跟别的女生怎么怎么样——>我们可以不怎么说话，我知道你一直在就行——>我喜欢你，做什么事都会想到你，好想找你

