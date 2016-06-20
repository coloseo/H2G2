# GitHub规范
### 参考资料
1. GitHub中文参考资料[链接](https://github.com/xirong/my-git/blob/master/how-to-use-github.md)
2. GitHub Flow流程描述[链接](https://guides.github.com/introduction/flow/)
3. GitHub风格markdown[链接](https://github.com/guodongxiaren/README)
> 以上文档是Github及git使用基础，请花时间阅读.

### 软件安装
1. 安装git 
> ```shell
> brew install git
> ```

2. 安装github for git toolkit
> ```shell
> brew install hub
> ```

### GitHub flow 介绍
GitHub flow 是简化的git flow,主要用于规范开发提交代码使用git及github的流程.  
## **重要的事情说三遍！！！**  
**不要在master分支直接提交代码!!!**  
**不要在master分支直接提交代码!!!**  
**不要在master分支直接提交代码!!!**  

#### GitHub flow流程简介  
![GitHub flow](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015122305.png)  
见上图，github开发流程主要分以下三个步骤:  
1. copy项目到本地,根据功能特性创建本地分支.  
2. 持续开发提交并同步到github远端仓库.  
3. 功能开发完成提交pull request.并对代码进行review通过以后merge进master分支  

光说不练假把式，直接上例子:  
1. 首先，在github上建立新仓库，仓库名称为H2G2(银河漫游指南)  
2. 设置好H2G2仓库master分支为保护状态  
3. 克隆仓库  
```shell
git clone git@github.com:coloseo/H2G2.git
```
4. 这时候产品经理二胡君，分配了一个任务给素还真:贤者，麻烦写一个Github规范文档.  
素还真首先要做的第一件事就是在本地先创建一个分支，分支名叫`github-doc`.创建分支代码如下:
```shell
git checkout -b github-doc
```
上面的命令相当于执行以下两条指令  
```shell
git branch github-doc
git checkout github-doc
```
先创建`github-doc`分支，再检出`github-doc`分支  
5.  素还真同学开始在该分支下开工了.  
> 2016-6-15日, 10点到14点，啪啦啪啦啪啦完成了文档的三分之一,可以提交一把了.
> ```shell
> git add . && git commit -m "素还真#2016-6-15 完成github command命令模块" && git push
> ```
> 2016-6-16日，10点到16点，啪啦啪啦完成了文档的三分之二, 又可以提交一把了.
> ```shell
> git add . && git commit -m "素还真#2016-6-16 完成github flow介绍部分" && git push
>```
> 2016-6-17日，10点到15点，啪啦啪啦终于把文档写完了.
> ```shell
> git add . && git commit -m "素还真#2016-6-17完成github-doc 功能" && git push
> ```
6. 素还真终于把文档写完了,下一步就是需要提交一个pull request到github.  
pull request 提交到github有两种方式:  
* low方式  打开github网站，访问相关项目并切换到pull request页面new一个新的pull request.
* big方式  使用之前的git命令行工具提交一个pull request.
```shell
git pull-request -m "素还真:完成Github文档编写"
```
7. 老司机一页书收到了素还真的pull reuquest请求,马上登录github去review代码.  
老司机不愧是老司机，马上发现了文档里面的一个错别字,`登录`写成了`登陆`,这还了得？ 一页书马上发起了一个issues.
```
git issue create -m "登录写成登陆了,差评！"
```

8. 素还真收到了老司机一页书review的结果，赶紧去查看，看了以后，心里不由深深的发起赞叹，老司机果然是老司机！  
素还真赶紧修改了issue,并重新提交了代码.  
```
git add . && git commit -m "closed#5 修复issue5,登陆已改成登录" && git push
```
9. 老司机一页书收到了素还真的提交，又仔细把代码review了一遍，嗯不错，通过！

10. 一页书把github-doc 分支代码部署到dev环境教给测试人员测试.

11. 测试通过后，合并分支到master并部署.
