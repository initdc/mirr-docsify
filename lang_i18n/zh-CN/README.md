# mirr.one

> 为开源的免费 CDN

[![gitlocalized ](https://gitlocalize.com/repo/7163/whole_project/badge.svg)](https://gitlocalize.com/repo/7163/whole_project?utm_source=badge)

## 概念

CDN 的优势可以用在包分发上，已经有使用的先例了，比如 npm、debian、alpine...

本项目旨在借助 CDN 改善部分开发者因网络问题而面临的困境

## 设计

域组合规则：

| 软件    | CDN 提供商 | 主域     |
| ------- | ---------- | -------- |
| ubuntu. | fastly.    | mirr.one |
| ubuntu. | fastly.    | mirr.one |

DNS 记录：

```dns
*.mirr.one.             1 IN CNAME workers.dev.  // Cloudflare’s 免费 SSL 证书覆盖主域及其二级子域名
*.gcdn.mirr.one.        1 IN CNAME cl-bec3d0f7.gcdn.co.
*.fastly.mirr.one.      1 IN CNAME nonssl.global.fastly.net.    // 开发者账户不能添加 SSL 证书
```

## 用法

例如 npm 注册表：

```sh
# 设定
npm config set registry https://npm.fastly.mirr.one

yarn config set registry https://npm.fastly.mirr.one


# 取消设定
npm config set registry https://registry.npmjs.org

yarn config set registry https://registry.npmjs.org
```

## 赞助商

| fastly CDN                                                                          |
| ----------------------------------------------------------------------------------- |
| <a href="https://www.fastly.com/"><img src="/_images/fastly.svg" width="120px"></a> |

## 提供者

- [Cloudflare](https://www.cloudflare.com/)
- [Fastly](https://www.fastly.com/)
- [G-core labs](https://gcorelabs.com/)
- [Netlify](https://www.netlify.com/)
- [fly.io](https://fly.io/)
- [Heroku](https://www.heroku.com/)

## lang_i18n Provider

- [gitlocalize](https://gitlocalize.com/)

## 许可协议

MPL-2.0
