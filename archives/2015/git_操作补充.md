#git 操作
###git 实际中的问题

1.创建一个裸仓库 git init --bare( **不创建分支**)，分支必须是被推送上去的   
2.创建一个文件夹，执行clone命令,   
	例如：git clone ssh://share@192.168.0.186/Users/share/Desktop/iosShare   
3. 添加文件，会自动生成master分支，   
4. git add --all   
5. git commit -m "xxx"   
6. git push origin master
7. git reset --hard 哈希值 回到之前版本
8. git log --since= "24 hours" -n 查看最近24小时的n条记录
   
```
创建其他分支(dev)也是一样的步骤，git push origin dev,第一次推送之前要合并master，不然master上的操作不会存在dev分支上   
 git merge master 
 git pull origin dev

```   

###附 git 基本操作   

###基本操作   1. 初始化仓库 git init   2. 配置作者信息    git config --global user.email "youremail@corp.com"    git config --global user.name "yourname"    
3. 添加文件到暂存区       git add <filename> git add * (添加所有文件到暂存区)    
4. 移除文件git rm <filename>    
5. 重命名一个文件git mv <oldfilename> <newfilename>    
6. 提交暂存区git commit 只会提交暂存区（staged）里面的文件git commit -m "message"       
7. 查看工作目录的状态    git status    
8. 查看提交历史记录     git log    
9. 查看文件改变 git diff   

###撤销操作1. 撤销加入暂存区的操作git reset HEAD <file>2. 撤销修改的操作git checkout -- <file>
3. 将本地的修改放进回收站 git stash4. 从回收站中恢复本地的修改 git stash apply   
###Tag操作 1. 查看tag    git tag2. 创建tag   git tag -a v1.0 -m "my version 1.0"   3. 显示tag信息   git show v1.0   4. 对之前的提交打tag   git tag -a v0.1 -m "version 0.1"   分支操作1. 查看分支git branch2. 创建分支git branch <branchname>3. 删除分支git branch -d <branchname>4. 切换分支git checkout <branchname>5. 合并分支git merge <branchname>6. rebase操作git rebase <basebranch> <newbranch>   

远端仓库操作   
   克隆一个远端仓库
 
```git clone URL 
```     添加远端仓库
```git remote add <name> <URL>
```   更新远端仓库的分支和数据   
 
```git fetch <name> 
```  
获取并合并远端仓库的分支到当前分支   
```      git pull <reponame> <branchname>eg: git pull origin master   
```
 上传本地分支和数据到远端仓库
   
```   git push <reponame> <branchname>       eg: git push origin master    

```   
 跟踪远端仓库上的分支

```git checkout --track origin/testbranch   
```￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼
￼