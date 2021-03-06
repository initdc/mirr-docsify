# mirr.one

> A free CDN for Open Source

[![gitlocalized ](https://gitlocalize.com/repo/7163/whole_project/badge.svg)](https://gitlocalize.com/repo/7163/whole_project?utm_source=badge)

## Concept

The advantages of CDN can be used in package distribution, and there are already precedents for using it, such as npm, debian, alpine...

This project aims to improve the plight of some developers due to network problems with the help of CDNs

## Design

Domain combination rule:

| Software | CDN provider | Main domain |
| -------- | ------------ | ----------- |
| ubuntu.  | fastly.      | mirr.one    |
| ubuntu.  | gcdn.        | mirr.one    |

DNS record:

```dns
*.mirr.one.             1 IN CNAME workers.dev.  // Cloudflare’s free SSL cert covered main domain and any 2nd level subdomain
*.gcdn.mirr.one.        1 IN CNAME cl-bec3d0f7.gcdn.co.
*.fastly.mirr.one.      1 IN CNAME nonssl.global.fastly.net.    // Developer account does not support add SSL certificates
```

## Usage

E.g. npm registry:

```sh
# set
npm config set registry https://npm.fastly.mirr.one

yarn config set registry https://npm.fastly.mirr.one


# unset
npm config set registry https://registry.npmjs.org

yarn config set registry https://registry.npmjs.org
```

## Sponsors

| fastly CDN                                                                          |
| ----------------------------------------------------------------------------------- |
| <a href="https://www.fastly.com/"><img src="/_images/fastly.svg" width="120px"></a> |

## Providers

- [Cloudflare](https://www.cloudflare.com/)
- [Fastly](https://www.fastly.com/)
- [G-core labs](https://gcorelabs.com/)
- [Netlify](https://www.netlify.com/)
- [fly.io](https://fly.io/)
- [Heroku](https://www.heroku.com/)

## lang_i18n Provider

- [gitlocalize](https://gitlocalize.com/)

## License

MPL-2.0
