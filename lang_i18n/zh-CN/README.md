# mirr.one

> 为开源的免费 CDN

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
*.mirr.one.             1 IN CNAME workers.dev.  // Cloudflare’s free SSL cert covered main domain and any 2nd level subdomain
*.gcdn.mirr.one.        1 IN CNAME cl-bec3d0f7.gcdn.co.
*.fastly.mirr.one.      1 IN CNAME nonssl.global.fastly.net.    // Developer account does not support add SSL certificates
```

## 用法

例如 npm 注册表：

```sh
# set
npm config set registry https://npm.fastly.mirr.one

yarn config set registry https://npm.fastly.mirr.one


# unset
npm config set registry https://registry.npmjs.org

yarn config set registry https://registry.npmjs.org
```

## 赞助商

| fastly CDN                                                                          |
| ----------------------------------------------------------------------------------- |
| <a href="https://www.fastly.com/"><img src="/_images/fastly.svg" width="120px"></a> |

## 提供者

- [Cloudflare](https://www.cloudflare.com/)
- [ Fastly](https://www.fastly.com/)
- [G-core labs](https://gcorelabs.com/)
- [ Netlify](https://www.netlify.com/)
- [fly.io](https://fly.io/)
- [Heroku](https://www.heroku.com/)

## 执照

MPL-2.0
