# Github release direct

## upstream

`github.com` release download

## example

```sh
wget https://github.com/egoist/bget/releases/download/v1.0.8/bget_1.0.8_Darwin_arm64.tar.gz
```

## official mirror

none

## local to our mirror

`gh-rel.fly.mirr.one`

`gh-rel.mirr.one` - Heroku docker

> `.heroku` is omitted

## usage

- Select manually

  1. get delivr url by access

     https://gh-rel.mirr.one/egoist/bget/releases/download/v1.0.8/bget_1.0.8_Darwin_arm64.tar.gz

  2. choose one of them
     ```sh
     wget https://obj-gh.fastly.mirr.one/github-production-release-asset-2e65be/420312993/8f3dd36c-a169-42fb-aad3-9e742cd63b4f?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20220206%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220206T192018Z&X-Amz-Expires=300&X-Amz-Signature=090b238b88a97163f597cd60e8ce994d52bf6277e24392a7256a290034dc9262&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=420312993&response-content-disposition=attachment%3B%20filename%3Dbget_1.0.8_Darwin_arm64.tar.gz&response-content-type=application%2Foctet-stream
     ```

- With query

  - fastly

    https://gh-rel.mirr.one/egoist/bget/releases/download/v1.0.8/bget_1.0.8_Darwin_arm64.tar.gz?fastly

    ```sh
    wget https://gh-rel.mirr.one/egoist/bget/releases/download/v1.0.8/bget_1.0.8_Darwin_arm64.tar.gz?fastly
    ```

  - gcdn

    https://gh-rel.mirr.one/egoist/bget/releases/download/v1.0.8/bget_1.0.8_Darwin_arm64.tar.gz?gcdn

    ```sh
    wget https://gh-rel.mirr.one/egoist/bget/releases/download/v1.0.8/bget_1.0.8_Darwin_arm64.tar.gz?gcdn
    ```
