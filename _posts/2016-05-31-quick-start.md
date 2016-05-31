---
layout: post
title:  "快速上手指南"
date:   2014-12-30 09:00:13
categories: jekyll update
permalink: /archivers/hello
---

# 快速上手指南

## 安装到 GitHub Pages

首先，你需要创建一个 GitHub Pages repo，[具体参考这里](https://pages.github.com/)。

然后再在你的电脑终端（或 Git Bash）一句句地运行下列指令。这将会下载 EasyBook 并上传到你的 repo。

```bash
git clone https://github.com/laobubu/jekyll-theme-EasyBook.git easybook
cd easybook
git remote add blog git@github.com:foo/bar #注1
git push -f -u blog gh-pages #注2
```

1. 修改 `git@github.com:foo/bar` 为[你的 git remote URL](https://help.github.com/articles/which-remote-url-should-i-use/)
2. 如果你的 repo 名字是 `xxxxx.github.io` 这种样子的，请将这一句换成以下两句指令：

```bash
git checkout -b master
git push -f -u blog master
```

## 配置

打开 `easybook` 文件夹并修改 `_config.yaml` 文件。

注意 `url` 和 `baseurl` 字段。假设你的网站地址是 `http://laobubu.github.io/`，使用

```yaml
url: "http://laobubu.github.io"
baseurl: ""
```

假设你的网站地址是 `http://laobubu.github.io/MarkdownIME/`, 用

```yaml
url: "http://laobubu.github.io"
baseurl: "/MarkdownIME"
```

你也可以使用[你自己的域名](https://help.github.com/articles/setting-up-a-custom-subdomain/)。

## 撰写文章

### 文件名和文件夹

文章应该保存在 `_posts` 文件夹。文件名遵循 `YYYY-MM-DD-TITLE.TYPE` 格式，例如：

- `2011-12-31-new-years-eve-is-awesome.md` *( md 意为 Markdown )*
- `2012-01-17-hello-world.md`

### YAML Front Matter

要让 Jekyll 正确地渲染你的帖子页面，请将 [YAML Front Matter](https://jekyllrb.com/docs/frontmatter/) 加到你的文章内容之前。例如这个最简短的例子：

```markdown
---
layout: post
title: Jekyll博客搭建指南
---

大家好，今天我要讲讲如何使用 EasyBook 这一个 Jekyll 主题搭建一个博客...
```

当然，你还可以设置[其他的变量](https://jekyllrb.com/docs/frontmatter/#predefined-global-variables)，就像这样：

```markdown
---
layout: post
title: Jekyll博客搭建指南
categories: 
 - 博客
 - 技术贴
permalink: /posts/1
nocomments: true  # 用于屏蔽评论区，为 EasyBook 专属功能。
---

大家好，今天我要讲讲如何使用 EasyBook 这一个 Jekyll 主题搭建一个博客...
```

### 了解更多

阅读 <https://jekyllrb.com/docs/posts/>

## 发布

使用 `git commit` 和 `git push`，就像往常一样提交到 GitHub。就这样。

## 升级你的 EasyBook

执行以下指令将自动获取并应用最新的 EasyBook 补丁：

```bash
git pull origin gh-pages
```

## 捐赠

如果你觉得 EasyBook 还不错的话，可以考虑包养我一顿饭钱，谢谢 :smiley: 

访问 <http://laobubu.net/donate.html> 捐赠页面
