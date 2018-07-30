# vuexdemo

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```
state 用来数据共享数据存储
mutation 用来注册改变数据状态，方法必须是同步方法
getters 用来对共享数据进行过滤操作
action 解决异步改变共享数据，包含任意异步操作

### 怎么处理多模块？

  应用简单，mutation、action、state各自定义一个总文件，如果多模块，那么在每个模块定义各自的这三个部分，借助vuex store的modules配置，子模块内开发体验跟原来的没差，也不需要关注它是否为一个子模块。
