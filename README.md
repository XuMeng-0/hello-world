# hello-world

## My first repository

### Study GitHub

### Study Git

#### Git 基础：远程仓库的使用

1. 查看远程仓库概要信息  
   `git remote`  
   `git remote -v`
2. 查看某个远程仓库的详细信息  
   `git remote show <remote>`
3. 添加一个远程仓库,并指定简写名称  
   `git remote add <shortname> <url>`  
   提示：`git clone` 命令会自动添加远程仓库
4. 重命名某个远程仓库  
   `git remote rename <name-current> <name-new>`
5. 从某个远程仓库中抓取与拉取  
    `git fetch <remote>`  
   注意：`git fetch` 命令只会将数据下载到本地仓库，而不会自动合并
6. 推送到某个远程仓库  
   `git push <remote> <branch>`
7. 移除某个远程仓库  
   `git remote remove <remote>`  
   `git remote rm <remote>`

#### Git 分支

分支基础

1. 分支创建  
   `git branch <branch-name-new>`
2. 分支切换：切换到一个已经存在的分支  
   `git checkout <branch-name>`
3. 分支创建切换：先创建分支，再切换到该分支  
   `git checkout -b <branch-name-new> `
4. 分支删除  
   `git branch -d <branch-name>`

分支进阶

1. 分支合并：将命令参数 `<branch-name>` 指定的分支合并到当前分支  
   `git merge <branch-name>`
2. 当目标分支所指向的提交是当前分支提交的直接后继时，快进（当前分支指针前移）
3. 当目标分支所指向的提交不是当前分支提交的直接后继时
    - 不冲突：使用两个分支的末端快照和它们的公共祖先进行三方合并，对合并结果创建提交，此提交被称为合并提交，它有两个父提交
    - 冲突：进行三方合并，手动解决冲突后标记为冲突已解决 `git add <file-name>`，手动创建合并提交

### Study markdown

## My name is xm.
