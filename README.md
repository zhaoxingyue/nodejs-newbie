# Nodejs Newbie


## 前端入门的4本书



- 精通CSS+DIV 网页样式与布局 http://product.china-pub.com/35553 
- 精通CSS：高级Web标准解决方案（第2版）http://product.china-pub.com/196593
- 锋利的jQuery(第2版) http://product.china-pub.com/3661548
- GitHub入门与实践 http://product.china-pub.com/4727673

第一本书是傻瓜式的入门的书，老点，但简单，符合国人思维，入门html和css比较合适

第二本书是css领域不错的书，加深理解css，努力成为一个合格的前端

第三本书是jquery的书，也是很简单，为啥没有直接javascript的原因是，jq足够简单，先实习效果，以后再慢慢补js基础即可，如果上来就js，很多人是搞不定的

第四本书是git和github的用法，是版本控制里比较简单的，比较适合入门

## 要求

- ubuntu
- sublime text3
- 编码风格 https://github.com/dead-horse/node-style-guide

## 安装nodejs

- 使用nvm安装多个版本（0.10.38必须装，其他自便）

 nvm  是nodejs version manager的缩写，即node版本管理工具，使用nvm能下载任意版本的nodejs

下载nvm，如果你使用git：


git clone https://github.com/creationix/nvm.git ~/.nvm && cd ~/.nvm && git checkout \`git describe --abbrev=0 --tags\`


下载完后：

```
source ~/.nvm/nvm.sh
```

这样你就能使用nvm 进行下载nodejs了，例如下载nodejs的稳定版本v0.12.5,输入以下命令：

```
nvm install v0.12.5
```

需要注意的是每次打开终端的时候并不能直接使用nvm,需要以下命令：

```
source ~/.nvm/nvm.sh
```

同时使用nvm能查看已安装的版本,使用以下命令:

```
nvm ls 
```

切换到想使用的某一个版本，例如切换到v0.12.5：

```
nvm use v0.12.5
```
查看当前的所有版本

```
nvm ls-remote
```

- 使用nrm切换源

nrm 是源管理器，用于切换NPM源，nrm能快速的通过命令切换，省去了手工切换的繁琐：
如下命令是查看NPM源：
```
nrm ls
```
显示如下源：

![](pic/zxy.png)

切换源使用：

```
nrm use 源名称
``` 

## Tips

### 编辑器

只允许文本编辑器，不准使用任何IDE

使用sublime的快速打开文件

    ctrl + p（mac是command + T）

在终端里使用subl命令打开文件，（如果是mac，需要安装https://github.com/i5ting/subl）

    subl app.js
  
快速定位到某一行

    ctrl + g （mac是command + L）


### 使用oh-my-zsh

- 官网 http://ohmyz.sh/
- 代码 https://github.com/robbyrussell/oh-my-zsh

安装步骤

- 先安装zsh
- 安装oh-my-zsh

以后环境变量在~/.zshrc里

### 安装ack，命令行查找代码

http://beyondgrep.com/install/


Ubuntu
    
- Package "ack-grep"

Mac

- brew install ack

### 使用autojump跳转目录

https://github.com/wting/autojump

Linux

    sudo apt-get install autojump
    
Mac os

    brew install autojump
    
需要修改~/.zshrc里的plugin,修改为

    plugins=(git autojump)

然后

    source ~/.zshrc
    
至此，已经完成了安装。

此后cd到任意目录，以后就可以使用j这个直达到某个目录了，下面是示例：

    ➜  nodejs-newbie git:(master) ✗ cd ~/workspace/github/nodejs-newbie
    ➜  nodejs-newbie git:(master) ✗ cd ~
    ➜  ~  j nodejs-n
    /Users/sang/workspace/github/nodejs-newbie
    ➜  nodejs-newbie git:(master) ✗ 
  
如果想玩的更high，可以参见https://github.com/clvv/fasd

### 使用mongo-express操作mongodb

<!-- https://github.com/andzdroid/mongo-express -->

<!-- 欢迎推荐ubuntu下更好的mongo客户端 -->

推荐 www.robomongo.org 

- 支持win
- 支持linux
- 支持mac（mac10.10下中文乱码，需要robomongo v0.8.5+）
 

### 使用node-inspector调试代码

https://cnodejs.org/topic/5463f6e872f405c829029f7e

### 使用mongoose-cli数据库建模

https://cnodejs.org/topic/55c44f0db98f51142b367b54

### 学习git用法

常用

	alias gs='git status'
	alias gp='git push'

使用alias来简化命令输入


- 重磅推荐peter wang写的 [搬进 Github](http://gitbeijing.com/)

下面给出一些git学习资料

- [git-guide](http://www.bootcss.com/p/git-guide/)
- [git入门gif演示](https://git.oschina.net/wzw/git-quick-start)
- [写出好的 commit message](http://ruby-china.org/topics/15737)
- [github-cheat-sheet](https://github.com/tiimgreen/github-cheat-sheet/blob/master/README.zh-cn.md)
- [分支管理](http://www.juvenxu.com/2010/11/28/a-successful-git-branching-model/)
- [Git-it Challenges is a terminal based app for learning Git and GitHub](http://jlord.github.io/git-it/)
- [高富帅们的Git技巧（译）](http://blog.csdn.net/zmlcool/article/details/8682382)
- [Git 怎样保证fork出来的project和原project（上游项目）同步更新](http://www.tuicool.com/articles/Mnmmqyi)
- [10.Git之本地忽略](http://blog.csdn.net/kangear/article/details/13169395)
- [git-flow 备忘清单](http://danielkummer.github.io/git-flow-cheatsheet/index.zh_CN.html)
- [Git flow 開發流程 ihower](http://ihower.tw/blog/archives/5140)
- [git bisect](http://www.oschina.net/translate/letting-git-bisect-help-you)

	$ git update-index --assume-unchanged /path/to/file       #忽略跟踪
	$ git update-index --no-assume-unchanged /path/to/file  #恢复跟踪
  
### 查询文档

- http://zealdocs.org/ (推荐，离线下载)

有很多doc在dash（mac）里默认是没有的；

see here ： http://kapeli.com/docset_links

如果是下载到本地的docset，放到zealdocs目录下面，需要重启zeal

### mongo here 

当前目录启动mongodb

在新建目录执行

    mh
    
它会创建tmp目录

全局启动mongodb

    mhg
    
它会创建~/mongo/目录，当前用户下起mongo服务，即用户下全局共享

https://github.com/i5ting/mongo-here

### json editor 

    [sudo] npm install -g je
    je

详见https://github.com/i5ting/je

### json to csv converter

    [sudo] npm install -g j2csv
    json2csv
    
详见https://github.com/i5ting/json2csv

上面给出的方案适合3000条以内的数据，受限于浏览器

更大量的数据，需要

    [sudo] npm install -g ej
    ej input.json output.csv
    
https://github.com/i5ting/ej

### kp is a tool for kill process by server port

    [sudo]npm install -g kp
    kp 3002

https://github.com/i5ting/kp

### upload-cli

a node cli tools for uploads ui

https://github.com/i5ting/upload-cli

- 目前已经支持通过命令行`uci`上传，可指定host

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request


## 版本历史

- v1.0.0 初始化版本

## 欢迎fork和反馈

- write by `i5ting` shiren1118@126.com

如有建议或意见，请在issue提问或邮件

## License

this repo is released under the [MIT
License](http://www.opensource.org/licenses/MIT).
