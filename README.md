# heroku-as-a-function [example]

<s>FAAS</s> Heroku as a Function (HAAF) runs your collection of request handlers without concerning you with the underlying server. Serverless? It's certainly less server.

## Functions
You write nodejs functions as [Koa](https://koajs.com/) request handlers.  See `functions/example.js`.
```js
const verb = 'get'
const path = '/'
const fctn = (ctx) => { ctx.body = "wubalubadubdub" }

module.exports = [verb, path, fctn]
```

## Auto-Scaling
Thanks to [Heroku Autoscaling](https://blog.heroku.com/heroku-autoscaling) your functions can dynamically grow/shrink inline with demand. Classic Heroku.

## Try it
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)
