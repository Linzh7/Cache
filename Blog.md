# 静态网站托管
## 原地址
https://github.com/lmk123/blog/issues/55#issue-231810320

## 常用的选择：GitHub Pages
### 优点
自带域名可 https 访问
可配置自定义域名
### 缺点
无法给自定义域名配置 SSL

## Bitbucket Cloud
跟 GitHub Pages 的功能一样，但是：

无法自定义域名
能且只能通过 https 协议访问（http 协议会被跳转到 https 协议）
所有项目的静态网站代码都只能放在专门的站点仓库里（accountName.bitbucket.io），不能像 GitHub 那样可以在每个项目里用 gh-pages 分支保存文件

## aerobatic
Bitbucket 旗下的静态网站托管服务。

可以使用 CLI 上传代码
支持自动构建（Continuous Deployment）
可以自定义域名但是是收费功能，自定义域名支持 https 且不需要提供证书，它会帮你生成一个

## GitLab Pages
同样跟 GitHub Pages 的功能一样，但是：

自定义域名可配置 https，不过需要上传证书

## surge.sh
只能使用 CLI 上传代码
支持自定义域名，但开启 SSL 是收费功能且需要自行上传证书
支持 200.html —— 适用于使用 History API 的 SPA

## Firebase Hosting
只能使用 CLI 上传代码
支持自定义域名并支持一键开启 https
支持重定向（Redirects）和重写（Rewrites）功能（当网站使用 History API 时特别有用
有被墙的风险……

## Netlify（推荐）
可以使用 CLI 上传代码
支持自定义域名且自定义域名支持一键开启 https（证书来自 Let's Encrype）
支持强制让用户通过 https 访问网站（开启后此功能后，http 的访问一律会 301 跳转到 https
支持自动构建
支持重定向（Redirects）和重写（Rewrites）功能
数据通过 HTTP2 协议传输
提供 webhooks 与 API

## now
可以使用 CLI 上传代码，或者链接一个 Git 仓库
不仅提供静态网站托管，同时也支持托管 Node.js 服务
支持自定义域名且自定义域名支持一键开启 https（证书来自 Let's Encrype）
数据通过 HTTP2 协议传输
提供 API

## 总结
推荐使用 Netlify，如果要顺便托管 Node.js 服务可以用 now。


# Hugo 添加 KaTeX支持
https://mertbakir.gitlab.io/hugo/math-typesetting-in-hugo/
