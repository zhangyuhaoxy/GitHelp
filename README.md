# GitHelp
Git Start 创建git步骤

单词解释 
index 缓存区
head 当前本地所指向的位置 也就是本地仓库
remote 远程主机列表
origin 默认远程主机名字(也就是远程仓库)
git fetch <远程主机名> <分支名> 取回远程主机的某某分支的更新在head 但不影响工作区代码 例如 git fetch origin master
git pull <远程主机名> <远程分支名>:<本地分支名> 取回远程主机的某某分支 应用到本地某某分支上 例如 git pull origin master:dev 取回远程master到本地dev上 不加:dev 为自动合并到当前分支

当新建项目时，或者clone之后新建立了另一个branche，不知道本地和远程的关系，那么需要进行建立追踪关系 git branch --set-upstream dev origin/dev 本地dev关联远程dev

1. 本地存在项目的话，进入项目目录，运行 
  git init
  初始化git

2. 到远程git仓库 or github 新建一个repositories 

3. 在本地项目运行
  git remote add origin https://github.com/zhangyuhaoxy/projet_name.git
  来进行关联
4. 继续运行
  git pull origin master
  把远程文件取回来
  
5. 然后进行git add commit 操作
  git add .
  添加全部文件到index
  git commit -m "second commit" 
  来传送到head
  git push origin master
  把head传送到远程remote
  
6. 以后进行 
  git add .
  git commit -m "third commit" 
  git push
  即可
  
  
最后 git 项目记录图形化输出 
git log --graph --decorate --pretty=oneline --abbrev-commit --all
