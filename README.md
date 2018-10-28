## hugo 的 yinwang.org 博客主题

<img style="width:69%" src="https://raw.githubusercontent.com/chinanf-boy/gohugo-theme-yinwang/master/images/tn.png">

<img style="width:80%" src="https://raw.githubusercontent.com/chinanf-boy/gohugo-theme-yinwang/master/images/screenshot.png">

### hugo 准备

若你第一次使用 hugo, 请参照一下[官方快速教程](https://gohugo.io/getting-started/quick-start/)

> [直到 _添加主题_ 那一步往下看](https://gohugo.io/getting-started/quick-start/#step-3-add-a-theme)

### 主题下载

0. 记得初始化

```bash
git init
```

1. 加入子模块

```
git submodule add https://github.com/chinanf-boy/gohugo-theme-yinwang.git themes/yinwang;
```

2. 主题设置

```
echo 'theme = "yinwang"' >> config.toml
```

2.1 加个文章

```
hugo new post/hello.md
```

> 最好再加个`about.md`

3. 服务器启动

```
hugo server -D
```

### config.toml 配置

```toml
baseURL = "http://example.org/"
languageCode = "en-us"
title = "我是"
theme = "yinwang"

[params]
    author = "yobrave Lee"
    github = "chinanf-boy"
    # gitlab = "yobrave"
    highlight = "dracula" # default use `github` style
    langs = ["go"]
    # 默认加载 highlight.min.js ，但 一些不支持的语言, 你自己添加

    # single = false
    # 单页面的Home 按钮去除
    # menus = true
    # 我 想加更多目录
```

## 常见问题

- **1. :** 我 想正常添加，更多目录

``` toml
[params]
    menus = true

[[menu.main]]
name = "分类"
url = "/categories/"

[[menu.main]]
name = "标签"
url = "/tags"

[[menu.main]]
  name = "Home"
  url = "/"
  # weight = 10 
# 这个权重，是衡量顺序的
``` 


> 提示：main的html顺序是相反的, 若想自定义顺序，添加 **权重值**


- **2. :** 我 想单页面的Home 按钮去除

``` toml
[params]
    single = false
``` 

### 本主题

是由[basics](https://github.com/arjunkrishnababu96/basics)hugo 主题, 拿来改的
