# Hexo-Theme-PureSuck

<div align="center">
<img alt="NPM Version" src="https://img.shields.io/npm/v/hexo-theme-puresuck?color=pink">
<img alt="GitHub License" src="https://img.shields.io/github/license/God-2077/hexo-theme-puresuck?color=pink">
<img alt="AUTHOR" src="https://img.shields.io/badge/author-Kissablecho-pink">
</div>

PureSuck，干净，纯洁，淡雅朴素的 Hexo 主题。

移植自 Typecho 主题 [PureSuck-theme](https://github.com/MoXiaoXi233/PureSuck-theme) ，感谢 MoXiify 开发了这么棒的一个主题。

## 注意

**遇到问题欢迎提 Issue。**

**遇到问题一定要提 Issue。**

## 演示

https://puresuck-demo.ksable.top/

### 安装与设置

安装主题

```bash
npm i hexo-theme-puresuck
```

博客根目录下的 `_config.yml` 文件通常负责站点相关配置、第三方 npm 插件相关的配置。

设置主题

```yaml
theme: puresuck
```

复制主题配置文件，运行下列代码

```bash
hexo copy_theme_config
```

关闭 Hexo 自带的代码高亮

`hexo >= 7.0.0`

```yaml
syntax_highlighter: # 留空
```

`hexo < 7.0.0`

```yaml
highlight:
  enable: false
```

### 页面

#### 文章头图

在 `Front-matter` 中设置 `img` 为文章头图的 `URL`，例如

```markdown
---
img: /images/MoXiiiiii.png
---
```

#### 文章摘要

在 `Front-matter` 中设置 `description` 为文章的摘要，例如

```markdown
---
description: 我是摘要
---
```

#### 归档页面

hexo 默认会在 `/archive` 下生成归档页面，你也可以在其他地方建立归档页面。

新建页面 `archive/index.md`

```markdown
---
layout: archive
title: 归档页面
---
```


## 功能与组件

#### 引用条
```
[alert type="red"]这是一个红色警告。[/alert]
[alert type="yellow"]这是一个黄色警告。[/alert]
[alert type="blue"]这是一个蓝色警告。[/alert]
[alert type="green"]这是一个绿色警告。[/alert]
[alert type="pink"]这是一个粉色警告。[/alert]
```
五种颜色可选，在 type 中填写，效果图可以看上面合集，普通的灰色样式用自带的 blockquote 即可
#### 彩色信息窗
```
[window type="red" title="信息窗口"]这是一个信息窗口。[/window]
[window type="yellow" title="警告窗口"]这是一个信息窗口。<br>这是一个信息窗口的第二行。[/window]
```
同样五色可选，type 处填写五种颜色之一，在 title 处填写标题，注意内部如果要换行请用`<br>`标签
#### 友链卡片
```
[friend-card name="好友" ico="avatar.jpg" url="http://example.com"]这是好友的描述。[/friend-card]
```
不可选择颜色，默认跟着主题强调色走的（在主题设置里切换），描述信息如果要换行请用`<br>`标签，描述信息尽量简短避免影响样式
#### 折叠内容
```
[collapsible-panel title="折叠面板标题"]这是面板的内容。[/collapsible-panel]
```
没有颜色选，灰色，用来折叠比较长的内容
#### Tabs选项组
```
[tabs]
[tab title="我的博客信息"]这是我的博客信息内容。[/tab]
[tab title="交流群"]这是交流群内容。[/tab]
[tab title="申请友链"]这有其他内容。[/tab]
[tab title="关于我们"]这是关于我们的内容。[/tab]
[/tabs]
```
按道理来说可以简单嵌套，简单测试了一下没什么问题
#### 时间线
```
[timeline]
[timeline-event date="2023-01-01" title="Event 1"]Description of Event 1.[/timeline-event]
[timeline-event date="2023-02-01" title="Event 2"]Description of Event 2.[/timeline-event]
[/timeline]
```
在[timeline]中添加子[timeline-event]一直加下去就行，应该没什么大问题
#### 视频卡片
目前只做了b站的
```
[bilibili-card bvid="BV1KJ411C7SB"]
```
像这样就可以插入一个视频卡片啦！其实就是官方那个 iframe 内嵌代码，更方便更简洁了一点而已，默认不自动播放
### *开发中的功能组件
#### 瀑布流图片
```
[PicGrid]
![图片.jpg][1]
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FGod-2077%2Fhexo-theme-puresuck.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FGod-2077%2Fhexo-theme-puresuck?ref=badge_shield)
[/PicGrid]
```
用 Typecho 默认的插入图片方式即可，用[PicGrid]标签包裹即可完成一个瀑布流的照片展示，适合多张图片展示的场景
#### MoxDesign
作为 JS 脚本在页面中自行开发使用  
需要使用的时候请确保在 DOMContentLoaded 之后调用  
MoxDesign Notification通知，默认出现在右下角
```
MoxNotification({
    title: "Persistent Notification",
    message: "This notification won't auto-close.",
    duration: 0, //设置为 0 则需要手动关闭，单位毫秒
});
```
MoxDesign Toast弹窗，等同切换颜色时的提醒
```
MoxToast({
    message: "This is a toast message",
    duration: 3000,
    position: "bottom", // 可以是 "top" 或 "bottom"
    backgroundColor: "var(--card2-color)",
    textColor: "var(--text-color)",
    borderColor: "var(--border-color)", // 使用CSS变量或默认值
});
```

## License

使用 GPL-3.0 协议开源，欢迎更多人参与二次开发！
感谢，每一个使用本主题的朋友们！


[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FGod-2077%2Fhexo-theme-puresuck.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FGod-2077%2Fhexo-theme-puresuck?ref=badge_large)