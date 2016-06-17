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
