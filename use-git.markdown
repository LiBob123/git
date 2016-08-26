##流行框架
###Git
- git是一款源代码管理工具。
###使用步骤：

### 初始化 
- 命令 `git init` 

### 设置个人信息
- 命令 `git config user.name ""` （局部用户信息）
- 命令 `git config user.email ""`
- 命令 `git config --global user.name ""` (全局用户信息）
- 命令 `git config --global user.email ""`

### 查看配置信息
- 命令 `git confit --list`

### 添加文件到暂存区
- 命令 `git add` 文件目录

### 提交得到仓库
- 命令 `git commit -m "注释"`

### 简写
批量添加文件到暂存区
命令 `git add .` (把当前目录下的所有文件添加到暂存区）
一次性添加文件到仓库（注意：只有之前有提交过的文件才能使用简写）
命令 `git commit -a -m "注释"`

### 忽略文件
以`.gitignore`命名一个文件
把要忽略的文件（以/开头文件名）写在.gitignore里就可以了。 例如：
/tmp.txt # 表示忽略根目录的tmp.txt文件
/js/*.js # 忽略js目录下所有js文件.

### 查看文件保存状态：
- 命令 `git status`

### 查看日志
- 命令 `git log`
- 命令 `git log --oneline` 查看简洁日志。

### 版本回退
- 命令 `git reset --hard Head~0
- 命令 `git reset --hard 版本号 版本号


### 查看所有操作日志
- 命令 `git reflog` 查看每一次操作的日志。

### 比较差异
- 命令 `git diff （比较工作区和暂存区文件的区别）
- 命令  git diff 版本号 版本号 想要比较的文件名 （比较指定文件的两个版本之间差别）

### Git 分支
- 命令 `git branch` 查看分支
- 命令 `git branch 分支名` 创建分支    
- 命令 `git checkout 分支名` 切换到指定分支 
- 命令 `git checkout -b 分支名` 创建分支并切换到该分支
- 命令 `git merge 分支名` 把指定的分支合并到当前分支上
- 命令 `git branch -d 分支名` 删除指定分支

## Github 和 Git
- github是一个网站, 提供了git服务器的功能
- git是版本管理工具

###上传代码到git服务器上

###推送到服务器上(push)
一个仓库是300M。
命令:git push [地址] [服务器上的分支名]
示例:git push https://github.com/huoqishi/test110.git master

###git clone
就相当于右键另存为,把项目中的代码下载下来.
命令:git clone [地址] [可以起个文件夹名]
示例:git clone https://github.com/huoqishi/test110.git test

###从服务器上拉取代码(pull)
有个条件，执行命令的目录必需有个仓库
使用github搭建个人博客
gh-pages,如果把代码上传到这个分支上就可以使用浏览器渲染访问。
访问的地址形式:[github用户名]github.io/[仓库名]/[具体的文件或者路径]

###创建远程服务器地址变量
命令:git remote add [变量名] [变量值]
创建之后就可以使用这个变量来代替地址使用.
在push时还可以加上-u参数，表示当前分支与指定的分支进行关联，下次push就不需要指定分支名了。