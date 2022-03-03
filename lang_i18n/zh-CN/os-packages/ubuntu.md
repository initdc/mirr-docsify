# ubuntu 软件包

## 上游

`archive.ubuntu.com`

## 官方镜像

https://launchpad.net/ubuntu/+archivemirrors

## 我们的镜像

`ubuntu.fastly.mirr.one`

`ubuntu.gcdn.mirr.one`

## 用法

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
