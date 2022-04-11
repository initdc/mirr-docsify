# Github 源

## 上游

`github.com`

## 示例

```sh
git clone https://github.com/element-plus/element-plus.git
```

## 官方镜像

没有

## 我们的镜像

- https

  `gh-cf.mirr.one`

  `gh.gcdn.mirr.one`

  `gh.fastly.mirr.one`

- ssh

  **![危险]   私钥将发送到镜像服务器, 请自己部署服务器**

  `ssh-fly.mirr.one`

  > ssh 代理 通过 caddy-l4, 源码: https://github.com/initdc/ssh-proxy-by-caddy-l4

## 浏览用途镜像

`gh-rep.mirr.one` -替换所有`.githubusercontent.com` 的跳转链接到 `-ghuser.mirr.one`, 由 Cloudflare Workers 驱动

## 用法

- 软件使用的仓库（例如 brew）

  https://coding.net

  从 github 导入 repo 作为镜像 repo，启用自动同步

- 人工管理

  `git clone`用 https，替换 url

  ```sh
  GIT_SSL_NO_VERIFY=1 git clone https://gh.gcdn.mirr.one/element-plus/element-plus.git

  cd element-plus

  git remote add github https://github.com/element-plus/element-plus.git
  ```

- ssh

  查看: https://github.com/initdc/ssh-proxy-by-caddy-l4#run
