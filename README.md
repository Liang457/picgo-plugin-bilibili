## picgo-plugin-bilibili

[![下载](https://img.shields.io/npm/dm/picgo-plugin-bilibili.svg?color=brightgreen)](https://npmcharts.com/compare/picgo-plugin-smms-user?minimal=true)
[![版本](https://img.shields.io/npm/v/picgo-plugin-bilibili.svg?color=brightgreen)](https://www.npmjs.com/package/picgo-plugin-smms-user)
[![许可](https://img.shields.io/badge/license-mit-brightgreen.svg)](https://github.com/xlzy520/picgo-plugin-smms-user/blob/master/License)


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

- 在线安装

  打开 [PicGo](https://github.com/Molunerfinn/PicGo) 详细窗口，选择**插件设置**，搜索**bili**安装，然后重启应用即可。

- 离线安装

  克隆该项目，复制项目到 以下目录：
    - Windows: `%APPDATA%\picgo\`
    - Linux: `$XDG_CONFIG_HOME/picgo/` or `~/.config/picgo/`
    - macOS: `~/Library/Application\ Support/picgo/`

  切换到新目录执行 `npm install ./picgo-plugin-bilibili`，然后重启应用即可。

### 获取B站SESSDATA

1. 登录[B站](https://www.bilibili.com/)
2. 按`F12`打开控制台
3. 找到`SESSDATA`复制即可

![](https://i0.hdslb.com/bfs/album/c78539a4883da29ed0dddfc0fa4e15057911e39d.png)



### 图片样式
可以参考[哔哩哔哩自己的](https://github.com/xlzy520/picgo-plugin-bilibili#%E5%9B%BE%E7%89%87%E6%A0%B7%E5%BC%8F)或 [Images.weserv.nl 的图片处理](https://images.weserv.nl/docs/)

### 解决B站防盗链（403）

[更加方便地解决B站防盗链 #5](https://github.com/xlzy520/picgo-plugin-bilibili/issues/5)

使用了 [Images.weserv.nl](https://images.weserv.nl/) 服务

会在输出时自动替换为经过 Images.weserv.nl 代理的图片，并且能过解决防盗链（要在设置选择哦）

就是在输出时的时候在链接前加上 `https://images.weserv.nl/?url=` (ps: 如果是 gif 动图还会在后面加入 `n=-1` 参数)