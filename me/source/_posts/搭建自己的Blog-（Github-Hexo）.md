---
title: 搭建自己的Blog （Github+Hexo）
date: 2016-12-21 11:12:45
tags:
  - hexo
  - github
---

        原来一直想搭建一个自己的网站，奈何考虑到要购买自己的域名，还有自己渣渣的前端水平，一直懒得没有做，今天看了些教程，落后啊。。。md转换就可以写blog。再说studio 、webstorm都可以装md插件，写blog那不是飕飕的了。我要踏上这条不归路，重在输出。
<!-- more -->
准备工作：

- **Node.js**
- **git**

-------------------

## 1.安装Hexo

- npm install -g hexo

## 2.初始化Hexo

 - hexo init

## 3.安装依赖包

 - npm install
## 4.生成静态页面

 - hexo generate
## 5.本地启动

 - hexo server    浏览器输入http://localhost:4000 即可查看
## 6.github方面的


 - 创建new repository，Repository name为：yourname.github.io（记得yourname就是你注册的github的用户名，是唯一的，别乱创建新的名称，除非你注册新的github）
 - 配置_config.yml  在deploy:添加
  type: git
  repo: 刚刚github创库地址.git  eg:https://github.com/xxxx/xxxx.github.io.git
  branch: master
 - npm install hexo-deployer-git --save
 - hexo deploy
 - 然后再浏览器中输入http://xxxx.github.io/就行了，譬如github的账户叫xxxx,把这个改成你github的账户名就行了


### 后续
每次部署的步骤，可按以下三步来进行。
    hexo clean
    hexo generate
    hexo deploy
一些常用命令：
hexo new"postName" #新建文章
hexo new page"pageName" #新建页面
hexo generate #生成静态页面至public目录
hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
hexo deploy #将.deploy目录部署到GitHub
hexo help # 查看帮助
hexo version #查看Hexo的版本



