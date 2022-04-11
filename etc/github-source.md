# Github source

## upstream

`github.com`

## example

```sh
git clone https://github.com/element-plus/element-plus.git
```

## official mirror

none

## our mirror

- https

  `gh-cf.mirr.one`

  `gh.gcdn.mirr.one`

  `gh.fastly.mirr.one`

- ssh

  **![DANGER] Private key will send to mirror server, deploy server by yourself**

  `ssh-fly.mirr.one`

  > ssh proxy by caddy-l4, source code: https://github.com/initdc/ssh-proxy-by-caddy-l4

## browsing mirror

`gh-rep.mirr.one` - replace all redirect URL of `.githubusercontent.com` to `-ghuser.mirr.one`, powered by Cloudflare Workers

## usage

- repo used by software (eg. brew)

  https://coding.net

  import repo as mirror repo from github, enable auto-sync

- Human managed

  `git clone` with https, replace url

  ```sh
  GIT_SSL_NO_VERIFY=1 git clone https://gh.gcdn.mirr.one/element-plus/element-plus.git

  cd element-plus

  git remote add github https://github.com/element-plus/element-plus.git
  ```

- ssh

  check: https://github.com/initdc/ssh-proxy-by-caddy-l4#run
