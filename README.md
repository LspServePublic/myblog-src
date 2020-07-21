# 个人博客  

## 搭建过程
1. 注册GitHub账号
2. 新建一个仓库，命名为`userName.github.io`
3. 本地安装**node.js**和**Git**
4. 进入gitbash输入以下命令检查安装是否成功
```shell
$ git version                 #检查git版本
$ node -v                     #检查node.js版本
$ npm -v                      #检查npm版本
```
5. 生成SSH添加到Github
```shell
$ git config --global user.name "userName" #设定用户名
$ git config --global user.email "userEmail" #设定用户邮箱
$ git config user.name #显示用户名
$ git config user.email #显示用户邮箱
$ git ssh-keygen -t rsa -C "userEmail" #输入用户邮箱创建sshkey，一路回车确定
```
6. 在GitHub中的Setting>Deploy keys点击Add deploy key，把本地用户文件夹下的.ssh文件夹中id_rsa.pub文件中的内容填入
7. 使用npm安装hexo
```shell
$ npm i hexo-cil -g #全局安装hexo，如果速度过慢可以换源或使用cnpm安装
$ npm config set registry https://registry.npm.taobao.org #换用淘宝源
$ npm install -g cnpm --registry=https://registry.npm.taobao.org #安装cnpm
```
8. 初始化一个项目
```shell
$ mkdir projectName #建立一个文件夹来存放项目
$ cd projectName #打开项目文件夹
$ hexo init #初始化hexo项目
$ npm install #安装依赖文件

```
## hexo 使用方法

```shell
$ hexo clean                  #清除缓存
$ hexo g || hexo generate     #生成静态页面
$ hexo s || hexo server       #启动本地服务
$ hexo d || hexo depoly       #推送到远程仓库
$ hexo new "new article name" #发表新文章
```

[markdown语法速查](./markdown语法速查.md)
