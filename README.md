## picgo-plugin-bilibili

[![许可](https://img.shields.io/badge/license-mit-brightgreen.svg)](License)

为 [PicGo](https://github.com/Molunerfinn/PicGo) 开发的一款插件，新增了[B站图床](https://bilibili.com/) 图床。
使用用户动态的图片上传API。填写`SESSDATA`即可，获取方式在下面。

### 目录
- [picgo-plugin-bilibili](#picgo-plugin-bilibili)
  - [目录](#目录)
  - [其他推荐](#其他推荐)
  - [安装](#安装)
  - [获取B站SESSDATA](#获取b站sessdata)
  - [图片样式](#图片样式)
  - [解决B站防盗链（403）](#解决b站防盗链403)

### 其他推荐
- [浏览器插件-Bilibili图床](https://github.com/xlzy520/bilibili-img-uploader)
- [Typora插件-Bilibili图床](https://github.com/xlzy520/typora-plugin-bilibili)

### 安装

- 离线安装

  克隆该项目，复制项目到 以下目录：
    - Windows: `%APPDATA%\picgo\`
    - Linux: `$XDG_CONFIG_HOME/picgo/` or `~/.config/picgo/`
    - macOS: `~/Library/Application\ Support/picgo/`

  切换到新目录执行 `npm install ./picgo-plugin-bilibili`，然后重启应用即可。

### 获取B站`SESSDATA``和csrf`

1. 登录[B站](https://www.bilibili.com/)
2. 按`F12`打开控制台
3. 找到`SESSDATA`复制即可
4. 找到`bli_jct`，填写进 `csrf` 即可

![](https://wsrv.nl/?url=https://article.biliimg.com/bfs/article/f8dacc0a76081764c07c1d40968e7423a970b89d.png)
![](https://wsrv.nl/?url=https://article.biliimg.com/bfs/article/9e0d900ffe53f2461e298af93a9390aaf6240df1.png)

### 图片样式
详见 [wsrv.nl的文档](https://wsrv.nl/docs/)

例如 `h=300` 会让图片等比例缩小至高度为300的图片再输出

### 解决B站防盗链（403）

[更加方便地解决B站防盗链 #5](https://github.com/xlzy520/picgo-plugin-bilibili/issues/5)

使用了 [wsrv.nl](https://wsrv.nl/) 服务

输出时替换为 wsrv.nl 的代理图片链接。可以绕过B站的防盗链，不过这个会让图片**加载速度变慢**。

就是在输出时的时候在链接前加上 `https://wsrv.nl/?url=` (如果是 gif 动图还会在后面加入 `n=-1` 参数)