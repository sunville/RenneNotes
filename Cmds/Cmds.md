# GPU info: 
##### 查看GPU信息
	$ nvidia-smi -q -g 0 -d UTILIZATION -l

# Git:
### 基本定义
* 工作区(working directory): 指的是你电脑中的路径，
* 版本库(repository): 指的是本地.git的隐藏目录，同事同步了云端
* 暂存区(stage/index): 属于版本库，接受工作区的内容（通过add），在通过commit更新到版本库对应的分支
* 远程仓库(对应github): 其实github是一个给git提供远程仓库的平台，先有git才有github	
### cmd方法 	
##### get git database from remote to local
	$ git clone [url] 
##### check the detail of your modification, 本地文件结构修改的详细状态
	$ git status
##### check the file status local modified and old version, 本地文件结构修改的简略情况
	$ git status -s 		
##### switch到对应的branch中去，-b表示新建branch
	$ git checkout [branch_name]
	$ git checkout -b [branch_name]
##### 放弃对这个file的修改，仅限在add之前
	$ git checkout --[file_name]
##### check the file change, 文件内容修改的情况
	$ git diff
##### 将文件修改添加到暂存区(stage)
	$ git add [file1] [file2]..
##### 删除，和Add操作类似
	$ git rm [file1] [file2]...
##### 重命名或者移动文件，同路径下重命名，非同路径则移动文件 
	$ git mv [file] [file/dir]
##### 将之前添加的文档reset到原来的未添加位置
	$ git reset HEAD [file1] [file2]...
##### 回到上一个版本，这个指令相当于修改HEAD的指针，HEAD^表示上一个版本，也可以指定版本
	$ git reset --hard HEAD^
##### 将暂存区内容提交到当前分支 (am表示add加modify)
	$ git commit -m ['commit log']	/ $git commit -am ['commit log']
##### 查看最近的commit的信息	\
	$ git log
##### 将云端代码库拉到本地代码库中，会自动merge，等于fetch+merge
	$ git pull
##### 将云端代码库拉到本地代码库中，不merge
	$ git fetch
##### 用于合并两个不同的分支
	$ git merge
##### 将本地commit过之后的修改放入云端代码库
	$ git push 

# vim
* 在vim中按ctl+z是强行退出，会留下修改缓存文件，正确不保存退出应该是:q!



# ls
##### 看隐藏文件
	$ ls -ah

