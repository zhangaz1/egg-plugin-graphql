# egg-plugin-graphql

[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![Test coverage][codecov-image]][codecov-url]
[![David deps][david-image]][david-url]
[![Known Vulnerabilities][snyk-image]][snyk-url]
[![npm download][download-image]][download-url]

[npm-image]: https://img.shields.io/npm/v/egg-plugin-graphql.svg?style=flat-square
[npm-url]: https://npmjs.org/package/egg-plugin-graphql
[travis-image]: https://img.shields.io/travis/nodejh/egg-plugin-graphql.svg?style=flat-square
[travis-url]: https://travis-ci.org/nodejh/egg-plugin-graphql
[codecov-image]: https://img.shields.io/codecov/c/github/nodejh/egg-plugin-graphql.svg?style=flat-square
[codecov-url]: https://codecov.io/github/nodejh/egg-plugin-graphql?branch=master
[david-image]: https://img.shields.io/david/nodejh/egg-plugin-graphql.svg?style=flat-square
[david-url]: https://david-dm.org/nodejh/egg-plugin-graphql
[snyk-image]: https://snyk.io/test/npm/egg-plugin-graphql/badge.svg?style=flat-square
[snyk-url]: https://snyk.io/test/npm/egg-plugin-graphql
[download-image]: https://img.shields.io/npm/dm/egg-plugin-graphql.svg?style=flat-square
[download-url]: https://npmjs.org/package/egg-plugin-graphql


Egg GraphQL 插件。


## 使用方法

### 安装

```bash
$ npm i egg-plugin-graphql --save
```


### 开启插件

```js
// config/plugin.js
exports.graphql = {
  enable: true,
  package: 'egg-plugin-graphql',
};
```

### 配置


```js
// config.default.js

// 配置 graphql
exports.graphql = {
  router: '/graphql',
  // 是否创建默认的空 schema
  defaultEmptySchema: false,
  // 是否加载开发者工具 (playground), 默认开启, 路由同 router 字段, 使用浏览器打开该可见
  playground: true,
};

// 使用 graphql 插件，拦截请求
exports.middleware = [ 'graphql' ];
```


## Example

- [example/simple](example/simple/) 一个简单的例子
- [example/modular-schema](example/modular-schema/) 模块化 schema

## GraphQL 实践系列文章

- [GraphQL 实践(一): GraphQL 简介](https://github.com/nodejh/nodejh.github.io/issues/51)

## 提问交流

请到 [issues](https://github.com/nodejh/egg-plugin-graphql/issues) 异步交流。

## License

[MIT](LICENSE)


