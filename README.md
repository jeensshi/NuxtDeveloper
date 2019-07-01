# Nuxt开发入门

## 基础知识

[TOC]



ECMA Script 合集

https://m.w3cschool.cn/wsqzg/



### 腾讯开发者手册

https://cloud.tencent.com/developer/doc/1270



### ECMAScript 6  

 http://es6.ruanyifeng.com/

主要学习Module部分内容

### WebPack

https://www.webpackjs.com/concepts/

js打包编译工具

==============================

### NPM

https://www.npmjs.com.cn/

包管理工具

或者 

### Yarn

https://yarn.bootcss.com/docs/

包管理工具

==============================

### VUE DevTools

https://github.com/vuejs/vue-devtools



### VUE CLI

https://cli.vuejs.org/zh/



### VUE Loader

https://vue-loader.vuejs.org/zh/



### VUE Router

https://router.vuejs.org/zh/



### VUEX

https://vuex.vuejs.org/zh/



### VUE SSR

https://ssr.vuejs.org/zh/



### NUXT

https://zh.nuxtjs.org/



### Element UI

https://element.eleme.io/#/zh-CN



## 补充知识

### Jest

https://jestjs.io/zh-Hans/

https://github.com/vuejs/vue-docs-zh-cn/blob/master/vue-cli-plugin-unit-jest/README.md

测试工具

### TypeScript

https://typescript.bootcss.com/

https://github.com/vuejs/vue-docs-zh-cn/blob/master/vue-cli-plugin-typescript/README.md



### Axios

https://www.kancloud.cn/yunye/axios/234845

https://www.npmjs.com/package/axios

异步通讯

### ESLint

https://cn.eslint.org/

https://eslint.org/

https://github.com/vuejs/vue-docs-zh-cn/blob/master/vue-cli-plugin-eslint/README.md



### Progressive web app (pwa)

https://developer.mozilla.org/zh-CN/docs/Web/Progressive_web_apps/App_structure

https://github.com/vuejs/vue-docs-zh-cn/blob/master/vue-cli-plugin-pwa/README.md



### Nightwatch

http://nightwatchjs.org/

https://github.com/vuejs/vue-docs-zh-cn/blob/master/vue-cli-plugin-e2e-nightwatch/README.md



### Prettier

https://prettier.io/



### Nodejs

http://nodejs.cn/

http://nodejs.cn/api/



### Normalize.css

http://necolas.github.io/normalize.css/



### Mockjs

http://mockjs.com/

生成随机数据，拦截 Ajax 请求

### Json Web Token

https://jwt.io/

用于身份验证

## Element UI 开发实例

https://panjiachen.github.io/vue-element-admin-site/zh/guide/



## Hello world

/assets/main.css

```css
.layout-enter-active, .layout-leave-active {
    transition: opacity .5s
}
.layout-enter, .layout-leave-active {
    opacity: 0
}
.page-enter-active, .page-leave-active {
    transition: opacity .5s
}
.page-enter, .page-leave-active {
    opacity: 0
}
```

/layouts/mylayout.vue

```vue
<template>
<el-container>
  <el-aside width="200px">Aside</el-aside>
  <el-container>
    <el-header><nuxt-link to="/">Head</nuxt-link></el-header>
    <el-main>
        <nuxt/>
    </el-main>
  </el-container>
</el-container>
</template>
<style>
body {
  height: 100%;
}
</style>
```

/pages/mypage.vue

```vue
<template>
<div><nuxt-link to="/secondpage">main</nuxt-link></div>
</template>
<script>
export default {
  layout: 'mylayout'
}
</script>
```

/pages/secondpage.vue

```vue
<template>
<div><nuxt-link to="/mypage">secondpage</nuxt-link></div>
</template>
<script>
export default {
  layout: 'mylayout'
}
</script>
```

/nuxt.config.js

```javascript
export default {
  layoutTransition: 'layout',
  transition: 'page',
}
```

## 使用技巧

### 安装Jquery库

```javascript
 npm install --save jquery
```

nuxt.config.js

```javascript
const webpack = require('webpack')
module.exports = {
	build: {

​```
    plugins: [
      new webpack.ProvidePlugin({
        '$': 'jquery'
      })
    ]
},
plugins: []
​```
}

```

