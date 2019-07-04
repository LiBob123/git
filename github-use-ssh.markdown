### 开启vscode git扩展
- 扩展程序——输入**@builtin**——找到git——启动——重启vscode
- 如果还是不能用看看用户配置 settings.json 中是否自定义配置关掉了 如`"git.enabled": false,` 改为true即可

### 配置git.path
- 进入settings.json
- 增加"git.path": "C:/Program Files/Git/bin/git.exe" (指向git安装目录)

### 生成SSH密钥
- 打开git bash 执行命令 `cd ~/.ssh` 
- 检查自己是否配置了user.name 和user.email 如果没有请先配置
- 可以使用命令 `ls` 查看之前是否有生成过密钥有的话直接用就好了
- 生成密钥 ssh-keygen -t rsa -C'xxx@xxx.com' 回车3次
- ssh目录下得到两个文件：id_rsa（私有秘钥）和id_rsa.pub（公有密钥）

### github 网址设置
- 如果想登陆远端，则需要将rsa.pub里的秘钥添加到远端。
- 登录自己的github账号进入setting
- 点击左边目录 SSH and GPG keys 然后创建New SSH key
- 标题可以设置提示自己（随意设置）  把rsa.pub复制进 key输入框 点击Add SSH key
- 再弹出窗口，输入你的GitHub密码，点击确认按钮，完工。
-  测试在命令窗口上输入    ssh -T git@github.com  按回车键，如看到以信息Hi xxx! You`ve successfully...
