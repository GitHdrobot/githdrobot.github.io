---
title: Build Your Blog
categories: Web Design
tags:
  - Hexo
  - Markdown
  - GitHub
---

# hexo 搭建github博客

## 准备工作

### GitHub账号

* 申请GitHub账号
* 创建username.github.io仓库

### 环境搭建

* 安装node.js
* 安装git

## 配置SSH key

* 在git bash中执行下面命令，连续回车3次

```shell
ssh-keygen -t rsa -C "邮件地址"
```
* 将文件~/.ssh/id\_rsa.pub文件中的公钥添加到GitHub中
* git bash 中执行下列命令，测试SSH配置是否正确

```shell
ssh -T git@github.com
```
* 设置邮箱、用户名

```shell
git config --global user.name "xxx"// xxx为github用户名
git config --global user.email  "xxx@163.com"// github注册邮箱
```
## 使用hexo写博客

### 什么是hexo

Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 [Markdown](http://daringfireball.net/projects/markdown/)（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

更多: [Get Started](https://hexo.io/docs/)

### hexo安装

```shell
npm install -g hexo-cli
hexo init
```
### hexo网站目录结构

```json
.
├── _config.yml             网站配置文件 
├── package.json            应用程序信息
├── scaffolds               模板文件夹
├── source                  资源文件夹
|   ├── _drafts
|   └── _posts
└── themes                  主题文件夹
```

# 编辑文档

* hexo new [layout] title                 创建文档，layout默认为post
* 使用编辑工具编辑创建的文档 
* hexo generate                             生成静态文件
* hexo clean && hexo deploy        部署到服务器

更多参见 [hexo doc](https://hexo.io/docs)

# hexo 升级

``` shell
npm install -g npm-check-updates
ncu
ncu -u
# 以下命令用来解决依赖问题，非必须，视实际环境执行
npm audit fix
npm audit
npm update kind-of --depth 10
```






