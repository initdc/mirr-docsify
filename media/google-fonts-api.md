# Google fonts api

## problem

Can't access `fonts.googleapis.com`

## example

```html
<html>
  <head>
    <link
      rel="stylesheet"
      href="https://fonts.googleapis.com/css?family=Tangerine"
    />
    <style>
      body {
        font-family: "Tangerine", serif;
        font-size: 48px;
      }
    </style>
  </head>
  <body>
    <div>Making the Web Beautiful!</div>
  </body>
</html>
```

## official mirror

not provide

## our mirror

`fonts-gapi.fib.one` provide by Cloudflare Workers

## usage

```html
<link rel="stylesheet" href="https://fonts-gapi.fib.one/css?family=Tangerine" />
```
