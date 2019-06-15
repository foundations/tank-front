## change default port to 6015
create file `vue.config.js` next to `package.json`
```js
module.exports = {
    devServer: {
        port: 6015
    }
}
```

## Add less support

npm install -D less-loader less

## Add http proxy

```
module.exports = {
  devServer: {
    proxy: {
      '/api': {
        //target: 'https://tank.eyeblue.cn',
        target: 'http://127.0.0.1:6010',
        changeOrigin: true,
        pathRewrite: {
          '^/api': '/api'
        }
      }
    }
  }
}
```

