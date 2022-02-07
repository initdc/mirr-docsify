# mirr.one

> A free CDN for Open Source

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
*.fastly.mirr.one.      1 IN CNAME j.sni.fastly.net.
*.gcdn.mirr.one.        1 IN CNAME cl-bec3d0f7.gcdn.co.
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

| fastly CDN                                                                         |
| ---------------------------------------------------------------------------------- |
| <a href="https://www.fastly.com/"><img src="_images/fastly.svg" width="120px"></a> |

## Providers

- [Fastly](https://www.fastly.com/)
- [Cloudflare](https://www.cloudflare.com/)
- [G-core labs](https://gcorelabs.com/)
- [Netlify](https://www.netlify.com/)
- [fly.io](https://fly.io/)
- [Heroku](https://www.heroku.com/)

## License

MPL-2.0
