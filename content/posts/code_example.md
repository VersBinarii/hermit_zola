+++
title="Code Example"
date=2020-06-13
draft=false

[taxonomies]
tags=["example"]
+++

## An Code example

Javascript code example.

```js
console.log('Hello World')
```

## Default NodeJS server

```js
const http = require('http')

const hostname = '127.0.0.1'
const port = 3000

const server = http.createServer((req, res) => {
  res.statusCode = 200
  res.setHeader('Content-Type', 'text/plain')
  res.end('Hello World\n')
})

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`)
})
```
