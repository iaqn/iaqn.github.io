# 🥰iaqn.github.io
🗓️我的hexo博客<br/>
✒️#2022年10月11日 时隔一年后的更新 
<hr/>
这不是新一年精弘技术部第一次例会的项目吗，恰逢我一个小学妹也要搭建自己的博客，干脆写篇教程。如果有幸发现这篇文章，可以按照如下教程进行操作

>主要参考一篇知乎文章https://zhuanlan.zhihu.com/p/102592286<br/>
>这里对这篇文章进行了勘误  由于本人计算机已经安装好了很多所需软件，以下从https://zhuanlan.zhihu.com/p/102592286 的第五篇——安装node.js和Hexo中安装Hexo的操作开始讲起

#### 1. 接下来就是安装Hexo，首先在D盘建立一个文件夹 Blog，以管理员身份运行cmd，并切换到D:\Blog，输入npm命令安装Hexo：
注意：不以管理员身份运行可能会出现报错情况
```
npm install -g hexo-cli
```
#### 2.安装完成后，输入 hexo init 命令初始化博客：
![1.png](./src/assets/images/1.png)
#### 3.然后输入 hexo g 静态部署：
![2.png](./src/assets/images/2.png)
#### 4.这时网页已经部署完成，输入 hexo s 命令可以查看,浏览器输入 http://localhost:4000 就可以打开新部署的网页,看完之后 ctrl +c 停止运行服务器
![3.png](./src/assets/images/3.png)
#### 5.将Hexo部署到GitHub,现在回到我们的 Blog 文件夹，打开 _config.yml 文件，下滑到文件底部，填上如下内容：
注意：这里填的是你的仓库地址，并且repository那里用ssh的地址带@符号的那个，如果用https有可能会报错，并且一定要注意空格
```
deploy:
  type: git
  repository: git@github.com:asfda/asfda.github.io.git #你的仓库地址
  branch: main
```
#### 6.继续使用我们先前打开的切换到D:Blog,具有管理员权限的cmd,安装Git部署插件，输入命令：
```
npm install hexo-deployer-git --save
```
#### 7.然后分别输入以下三条命令：
```
hexo clean   #清除缓存文件 db.json 和已生成的静态文件 public
hexo g       #生成网站静态文件到默认设置的 public 文件夹(hexo generate 的缩写)
hexo d       #自动生成网站静态文件，并部署到设定的仓库(hexo deploy 的缩写)
```
完成以后，打开浏览器，输入 https://xxx.github.io 就可以打开你的网页了：
现在虽然可以访问我们的网站，但是网址是GitHub提供的：http://xxxx.github.io 而我们想使用我们自己的个性化域名，这就需要绑定我们自己的域名。

<hr/>

## 第六篇 解析域名 请参考 https://zhuanlan.zhihu.com/p/103813944
1.注意：在获取你的仓库的IPV4地址时 需要ping + 你的GitHub的网址+ -4
例如：
```
ping fengye97.github.io -4
```
2.注意(摘自评论)：如果一切配置没有错误，还显示404的话，建议验证手机版输入你的个人域名，如果手机版可以显示而电脑版无法显示的话，只需要清除你浏览器的缓存即可。如果手机/电脑端都无法显示：1.再次验证指向是否有错误 2.毫无错误，修改dns记录服务器需要一定延时来处理的，所以等待一会再验证。除此之外，os系统不需要添加两个lz添加的文件夹
<br/>
3.如果手机端有用，电脑端域名输入无法加载网页的话，有一定延迟，等个十来分钟二十来分钟就好了<br/>
4.用git bash操作的，可以在cmd上来完成

## 💻 至此，一个`**最基本**`的博客就搭好了，关于后续页面美化和编写，就要依靠自己的技术了，当然导入模版可能更容易。但博客嘛，肯定要有自己的特色~
`祝各位`🚀🚀🚀 期待各位的博客哟~
可以继续参考https://zhuanlan.zhihu.com/p/102592286 的第七、第八篇
