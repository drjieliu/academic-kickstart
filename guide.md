## 个人网站修改指南

- [个人网站修改指南](#个人网站修改指南)
  - [准备软件](#准备软件)
  - [元文件结构](#元文件结构)
  - [修改步骤](#修改步骤)

### 准备软件

1. Git

2. Hugo [下载链接](https://github.com/gohugoio/hugo/releases/download/v0.74.3/hugo_extended_0.74.3_Windows-64bit.zip)

### 元文件结构
网站内容编辑使用markdown格式

**关键内容路径**

config/_default/menus.toml 菜单配置

content/authors/admin/_index.md 个人简介配置

content/home/experience.md 个人经历

content/home/academic-service.md 学术服务

content/home/publications.md 期刊

### 修改步骤
1. clone 代码库 https://github.com/drjieliu/academic-kickstart.git

```bash
git clone https://github.com/drjieliu/academic-kickstart.git
cd academic-kickstart
git submodule update --init --recursive
```

1. 在代码库根目录运行之前下载的hugo工具，并执行hugo server，可以在本地实时预览最新修改.

2. 本地浏览器打开http://localhost:1313预览网站内容

3. 修改后完成后在根目录执行hugo命令手动生成网站内容, public目录为hugo工具生成的网站静态文件
```bash
hugo
cd public
git add .
git commit -m "Build website"
git push origin master
cd ..
```

4. 修改后提交网站元内容
```bash
git add .
git commit -m "modify content"
git push origin master
cd ..
```