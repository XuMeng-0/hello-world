# hello-world

## Study GitHub

## Study Git

### Git 起步：配置

1. 三个配置文件

    - `git config --system` `etc/gitconfig` 系统上每个用户及其仓库的通用配置
    - `git config --global` `~/gitconfig` 当前用户及其所有仓库的通用配置
    - `git config --local` `.git/gitconfig` 当前仓库的配置，生效条件：在某个仓库中

2. 查看配置信息
    - 查看所有配置:可能会看到重复变量，此时会使用最后一个配置  
      `git config --list`
    - 查看所有配置及其所在文件  
      `git config --list --show-origin`
    - 查看某一项配置  
      `git config <key>`

### Git 起步：帮助

1. 查看 Git 命令的综合手册  
   `git help <verb>`  
   `git <verb> --help`
2. 查看 Git 命令的简明参考  
   `git <verb> -h`

### Git 基础：获取 Git 仓库

1. 方式一：将尚未进行版本控制的本地目录转换为 Git 仓库

    - 进入项目目录
    - `git init` 它会创建 .git 子目录，其中的文件是 Git 仓库的骨干
    - `git add <file-name>` 指定需要进行追踪的文件
    - `git commit` 进行初始提交

2. 方式二：从其他服务器克隆一个已存在的 Git 仓库
    - 克隆远程仓库  
      `git clone <url>`
    - 克隆远程仓库，并定义本地仓库名  
      `git clone <url> <local-repository-name>`

### Git 基础：记录每次更新到仓库

1. 检查当前文件状态
    - 详细 `git status`
    - 简洁 `git status --short`
    - 简洁 `git status -s`
2. 跟踪新文件  
   `git add <files>`
    - 命令参数：文件或目录路径
    - 目录的路径作为参数时，将递归地跟踪该目录下的所有文件
3. 暂存已修改的文件  
   `git add <files>`  
   `git add ` 命令的功能
    - 开始跟踪新文件
    - 把已跟踪的文件放到暂存区
    - 合并分支时，把有冲突的文件标记为已解决状态
4. 忽略文件
    - 用途：使无需纳入 Git 管理的文件不再出现在未跟踪文件列表
    - 文件名: .gitignore
    - 常见的需要忽略的文件：日志文件，编译过程中创建的临时文件
5. 查看已暂存和未暂存的修改
    - 查看未暂存文件的更新  
      `git diff`
    - 查看已暂存文件的更新  
      `git diff --staged`  
      `git diff --cached`
6. 提交更新
    - `git commit`
    - `git commit -m <commit-message>`
7. 跳过使用暂存区  
   `git commit -a`
8. 移除文件
    - 从 Git 仓库和当前目录中删除指定文件  
      `git rm <file-name>`
    - 从 Git 仓库和当前目录中删除指定文件，该文件修改后尚未提交  
      `git rm -f <file-name>`
    - 从 Git 仓库中删除，但保留在当前工作目录中  
      `git rm --cached <file-name>`
9. 移动文件  
   `git mv <file-from> <file-to>`

### Git 基础：远程仓库的使用

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

### Git 分支

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

1. 分支合并  
    命令：将命令参数 `<branch-name>` 指定的分支合并到当前分支  
   `git merge <branch-name>`  
    当目标分支所指向的提交是当前分支提交的直接后继时，快进（当前分支指针前移）  
    当目标分支所指向的提交不是当前分支提交的直接后继时
    - 不冲突：使用两个分支的末端快照和它们的公共祖先进行三方合并，对合并结果创建提交，此提交被称为合并提交，它有两个父提交
    - 冲突：进行三方合并，手动解决冲突后标记为冲突已解决 `git add <file-name>`，手动创建合并提交
2. 变基  
   定义：将提交到某个分支上的修改移到另一个分支上  
   用处：使提交历史更加整洁  
   使用变基需要遵守的规则：只对尚未分享给别人的修改执行变基操作  
   命令：将当前分支变基到目标基底分支  
   `git rebase <target-branch>`

### Git 工具

1. 贮藏  
   使用场景：希望切换到其他分支处理问题，又不想为当前的工作状态创建一次提交。  
   命令：
    - 贮藏当前状态  
      `git stash push`
    - 应用最近的贮藏  
      `git stash applay`
    - 移除贮藏  
      `git stash drop`
    - 应用并移除贮藏  
      `git statsh pop`

## Study markdown

## My name is xm.
