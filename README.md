# vue_spa

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### 设置less全局变量
```
1、安装loader包
npm i style-resources-loader vue-cli-plugin-style-resources-loader -D 
 或 
yarn add style-resources-loader vue-cli-plugin-style-resources-loader -D

2、配置vue.config.js
const path = require("path");
module.exports = {
  ...
  pluginOptions: {
  "style-resources-loader": {
    preProcessor: "less",
    patterns: [
      //这个加上自己的路径，  注意：试过不能使用别名路径
      path.resolve(__dirname, "./src/assets/variable.less")
      ]
    }
  }
  ...
}
```

### 设置@2x图片dpr自适应
```
1、查看common/css/variable.less文件定义变量，基于@media

2、在less全局变量配置成功的情况下可以在任意vue组件中直接使用变量
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
