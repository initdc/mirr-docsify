# Backblaze B2

## 上游

```js
f001.backblazeb2.com;
f002.backblazeb2.com;
f003.backblazeb2.com;
f004.backblazeb2.com;
```

## 示例

```md
![avatar](https://f002.backblazeb2.com/file/backend1/14258692.png)
```

## 官方镜像

没有

## 我们的镜像

- [带宽联盟 - Backblaze | Cloudflare](https://www.cloudflare.com/zh-cn/bandwidth-alliance/backblaze/)

  ```js
  f001.mirr.one;
  f002.mirr.one;
  f003.mirr.one;
  f004.mirr.one;
  ```

- [使用 Backblaze B2 进行数据传输 |快速帮助指南](https://docs.fastly.com/en/guides/data-transfer-with-backblaze-b2)

  ```js
  // Not support https, only for downloading resource
  // Don't use it for providing website resource

  f001.fastly.mirr.one;
  f002.fastly.mirr.one;
  f003.fastly.mirr.one;
  f004.fastly.mirr.one;
  ```

## 用法

替换网址

> **![WARNING] 不要使用多线程下载器下载资源，这会消耗大量的请求配额。**

![B2 警告](/_images//b2-warning.jpg)
