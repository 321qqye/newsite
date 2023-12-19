+++
title = 'First'
date = 2023-12-12T09:41:07+08:00

+++

## 创建 Hugo 内容

方法一：使用 hugo new content 命令创建，其中最后的参数为`hugo new content /posts/first.md`
方法二：人工创建，使用 VS Code 编辑器，在`content`目录中创建`posts`目录，然后在`posts`目录中新建后缀名为`.md`的文件即可。

## 使用 Markdown 语法编辑页面内容

Markdown 是一种非常容易学习的标记语言，规则见：<https://www.markdownguide.org/cheat-sheet/>

必须掌握的有：超级链接、图片、视频、标题、段落

### 超级链接

超级链接的语法为`[]()`，方括弧中的为链接内容，圆括弧中为链接地址。

[西北民族大学](https://www.xbmu.edu.cn)是新中国第一所民族高等教育院校。

### 图片

图片的标记语法为`![]()`，方括弧中的内容为图片描述文字，圆括弧中为图片的地址，可以是在线地址，也可以是本地地址。

![markdown](https://pic2.zhimg.com/v2-163d0abaa24c39440d53b080ca4b6c7a_r.jpg)

![markdown](/images/markdown.jpg)

### 视频

视频内容，建议上传到视频网站，例如优酷、B 站，然后使用这些网站的分享嵌入功能，利用`iframe`元素实现视频的播放。

<iframe src="//player.bilibili.com/player.html?aid=834386267&bvid=BV1G34y1F7nZ&cid=1359032219&p=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="800px" height="600px"> </iframe>

默认情况下，Hugo 工具是不支持在 markdown 中使用 html 内容的，但是可以通过设置让其支持 html，在 hugo 配置中增加如下内容即可：

```
[markup]
defaultMarkdownHandler = "goldmark"
[markup.goldmark]
[markup.goldmark.renderer]
unsafe = true
```

对于播放器的样式，支持 CSS 的样式设置。例如:

```html
<iframe
  src="//player.bilibili.com/player.html?aid=834386267&bvid=BV1G34y1F7nZ&cid=1359032219&p=1"
  scrolling="no"
  border="0"
  frameborder="no"
  framespacing="0"
  allowfullscreen="true"
  width="800px"
  height="600px"
>
</iframe>
```

使用 iframe 还可以嵌入其他类型的页面。

<iframe id="embed_dom" name="embed_dom" frameborder="0"  src="https://www.processon.com/embed/611dc2081efad457f1838bb5" style="width:400px"></iframe>
