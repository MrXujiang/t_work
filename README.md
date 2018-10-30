# client-web

> Nuxt.js project

## Build Setup

``` bash
# install dependencies
$ npm install # Or yarn install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout the [Nuxt.js docs](https://github.com/nuxt/nuxt.js).

## 总结

### 1. 报错解决方案

``` js
// 错误一：events.js:183  throw err; Unhandled 'error' event
一般都是端口被占用，解决占用即可
```

### 2. 样式

``` css
/* 激活链接样式 */
设置激活链接样式时为了去除前一个激活链接的样式，应设置此类名的样式：.nuxt-link-exact-active

/* 全局使用less */
[参考链接](https://github.com/nuxt/nuxt.js/tree/dev/examples/style-resources)

/* 给页面或组件写样式时一定要限定作用域 scoped, 否则可能出现样式混乱 */
```
