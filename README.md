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
*.fastly.mirr.one.      1	IN	CNAME	j.sni.fastly.net.
*.gcdn.mirr.one.        1	IN	CNAME	cl-bec3d0f7.gcdn.co.
```

## Usage

E.g. ubuntu:

```sh
sudo su

## http
# set
sed -i 's/archive.ubuntu.com/ubuntu.fastly.mirr.one/g' /etc/apt/sources.list
sed -i 's/security.ubuntu.com/ubuntu-sec.fastly.mirr.one/g' /etc/apt/sources.list

# unset
sed -i 's/ubuntu.fastly.mirr.one/archive.ubuntu.com/g' /etc/apt/sources.list
sed -i 's/ubuntu-sec.fastly.mirr.one/security.ubuntu.com/g' /etc/apt/sources.list


## https need  ca-certificates  installed
# set
sed -i 's/http:\/\/archive.ubuntu.com/https:\/\/ubuntu.fastly.mirr.one/g' /etc/apt/sources.list
sed -i 's/http:\/\/security.ubuntu.com/https:\/\/ubuntu-sec.fastly.mirr.one/g' /etc/apt/sources.list

# unset
sed -i 's/https:\/\/ubuntu.fastly.mirr.one/http:\/\/archive.ubuntu.com/g' /etc/apt/sources.list
sed -i 's/https:\/\/ubuntu-sec.fastly.mirr.one/http:\/\/security.ubuntu.com/g' /etc/apt/sources.list
```

## Sponsors

- [Fastly](https://www.fastly.com/)

## Providers

- [Fastly](https://www.fastly.com/)
- [Cloudflare](https://www.cloudflare.com/)
- [G-core labs](https://gcorelabs.com/)
- [Netlify](https://www.netlify.com/)

## License

MPL-2.0
