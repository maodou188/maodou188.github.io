+++
title = 'Chrome 浏览器使用 Cookie 登录 Facebook'
description = 'Chrome 浏览器使用 Cookie 登录 Facebook，可实现无账号密码一键登录 Facebook。'
date = 2025-08-08T06:52:00
draft = false
+++
 
### 前提条件

1. 电脑已安装好 Chrome 浏览器（能访问 Google）
3. 安装插件`Cookie Editor`
	* 使用 Chrome 浏览器，点击链接安装： [**安装插件 Cookie-Editor**](https://chromewebstore.google.com/detail/cookie-editor/hlkenndednhfkekhgcdicdfddnkalmdm?hl=zh-CN)

3. 一个可用的 Facebook 账号，且带 Cookie
	* 只需要两个必须的 Cookie: `xs`、`c_user`，其他的可有可无
 


### Cookie 的格式

在导入 Cookie 之前先说一下 Cookie 两种格式：

1. JSON 格式

```JSON
[{
	"name": "c_user",
	"value": "61577773708449",
	"expires": "Wed, 24 Jun 2026 04:36:51 GMT",
	"expires_timestamp": 1782275811,
	"domain": ".facebook.com",
	"path": "/",
	"secure": true,
	"httponly": null,
	"samesite": "None"
}, {
	"name": "xs",
	"value": "xxx",
	"expires": "Wed, 24 Jun 2026 04:36:51 GMT",
	"expires_timestamp": 1782275811,
	"domain": ".facebook.com",
	"path": "/",
	"secure": true,
	"httponly": true,
	"samesite": "None"
}]
```
**注意：如果JSON中有转义符号`\`需要去掉，如path部分可能是`\/`，实际是`/`**

2. URL 格式

```txt
c_user=61577773708449; xs=xxx
```

以上两种格式，`Cookie-Editor` 都支持。

### 导入 Cookie 

1. 使用 Chrome 浏览器打开 [Facebook](https://www.Facebook.com]
2. 使用 `Cookie-Editor` 导入 Cookie
3. 导入成功后，刷新网页就登录成功了

{{< video "media/video.mp4" >}}



