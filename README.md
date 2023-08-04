Nuxt.js
## 一、为什么要用Nuxt.js
原因其实不用多说，就是利用Nuxt.js的服务端渲染能力来解决Vue项目的SEO问题。
## 二、Nuxt.js和纯Vue项目的简单对比
1. build后目标产物不同
vue: dist
nuxt: .nuxt
2. 网页渲染流程
vue: 客户端渲染，先下载js后，通过ajax来渲染页面；
nuxt： 服务端渲染，可以做到服务端拼接好html后直接返回，首屏可以做到无需发起ajax请求；
3. 部署流程
vue： 只需部署dist目录到服务器，没有服务端，需要用nginx等做Web服务器；
nuxt： 需要部署几乎所有文件到服务器（除node_modules，.git），自带服务端，需要pm2管理（部署时需要reload pm2），若要求用域名，则需要nginx做代理。
4. 项目入口
vue: /src/main.js，在main.js可以做一些全局注册的初始化工作； nuxt: 没有main.js入口文件，项目初始化的操作需要通过nuxt.config.js进行配置指定。
五、最后
Nuxt.js引入了Node，同时nuxt.config.js替代了main.js的一些作用，目录结构和vue项目都稍有不同，增加了很多的约定，对于初次接触的同学可能会觉得非常陌生，更多的内容还是得看一遍官方的文档。
demo源码: fengxianqi/front_end-demos/src/nuxt-test。

<!-- https://github.com/fengxianqi/front_end-tools.git -->