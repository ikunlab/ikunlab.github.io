---
title: 多人协作
---

## Previously (前情提要)

* 方法参考 https://blog.csdn.net/Yongzili/article/details/98535710
* 【重要】源文件在 Hexo 分支，博客文件在 main 分支

### 拉取仓库并初始化

``` bash
git pull git@github.com:ikunlab/ikunlab.github.io.git
cd ikunlab.github.io
ls
git branch -a
git switch Hexo
ls
npm install hexo && npm install && npm install hexo-deployer-git #（不需要hexo init）
```

### 更新文章

* 同步下仓库先

``` bash
git pull origin Hexo
```

* 编辑source文件夹内的md后，运行

``` bash
#同步源文件
git add .
git commit -m "文字描述"
git push origin Hexo 

#更新博客
hexo clean && hexo g -d
```
