# 1. 准备工作
## 1.1. node.js环境（npm包管理器）
- node.js下载地址：[node.js官网](https://nodejs.org/en/download/)
用中文网比较下载比较快：[快速下载node.js](http://nodejs.cn/download/)
```
node -v 
npm -v
输入命令之后出现版本后就算成功安装
```
## 1.2. vue-cli 脚手架构建工具
- 推荐使用国内镜像来安装，所以我们先设置 cnpm：
```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```
- 如果安装失败，可以使用 npm cache clean清理缓存，然后再重新安装。后面的安装过程中，如有安装失败的情况，也需要先清理缓存

- 同样可以使用cnpm -v 查看是否安装成功
## 1.3. cnpm  npm的淘宝镜像
```
npm i -g cnpm --registry=https://registry.npm.taobao.org
npm i -g vue-cli
```
- 测试是否安装成功：
```
vue -V
```
## 1.4. 开发运行

```
    # 安装依赖
    npm install
    //or # 建议不要用cnpm  安装有各种诡异的bug 可以通过如下操作解决npm速度慢的问题
    npm install --registry=https://registry.npm.taobao.org

    # 本地开发 开启服务
    npm run dev
```
浏览器访问 http://localhost:9527

# 2. 目录结构
```shell
├── build                      // 构建相关  
├── config                     // 配置相关
├── src                        // 源代码
│   ├── api                    // 所有请求
│   ├── assets                 // 主题 字体等静态资源
│   ├── components             // 全局公用组件
│   ├── directive              // 全局指令
│   ├── filtres                // 全局filter
│   ├── mock                   // mock数据
│   ├── router                 // 路由
│   ├── store                  // 全局store管理
│   ├── styles                 // 全局样式
│   ├── utils                  // 全局公用方法
│   ├── view                   // view
│   ├── App.vue                // 入口页面
│   └── main.js                // 入口 加载组件 初始化等
├── static                     // 第三方不打包资源
│   ├── jquery
│   └── Tinymce                // 富文本
├── .babelrc                   // babel-loader 配置
├── eslintrc.js                // eslint 配置项
├── .gitignore                 // git 忽略项
├── favicon.ico                // favicon图标
├── index.html                 // html模板
└── package.json               // package.json

```

# 3. 状态管理
后台只有user和app配置相关状态使用vuex存在全局，其它数据都由每个业务页面自己管理。

# 4. 感谢
感谢作者：[PanJiaChen](https://github.com/PanJiaChen/vue-element-admin)
