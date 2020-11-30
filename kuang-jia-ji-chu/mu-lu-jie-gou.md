# 目录结构

```
cloudfunctions/ - 云函数目录(阿里云为aliyun,腾讯云为tcb,详见uniCloud - https://uniapp.dcloud.io/uniCloud/)
componets/ - 符合vue组件规范的uni-app组件目录
│  └─comp-a.vue - 可复用的a组件
hybrid/ - 存放本地网页的目录 - https://uniapp.dcloud.io/component/web-view
platforms/ - https://uniapp.dcloud.io/platform?id=整体目录条件编译
pages/ - 页面文件路由目录
    index/ - 默认首页
        index.vue
static/ - 存放应用引用静态资源(如图片、视频等)的目录,注意:静态资源只能存放于此
wxcomponents/ - 存放小程序组件的目录 - https://uniapp.dcloud.io/frame?id=小程序组件支持
unpackage/ - 编译打包目录
    dist/
      dev/ - 测试目录
        app-plus - 手机端
        mp-weixin - 微信小程序
      build - 编译过后的目录
App.vue - 应用配置,用来配置App全局样式以及监听 - https://uniapp.dcloud.io/frame?id=应用生命周期
main.js - Vue初始化入口文件
manifest.json - 配置应用名称、appid、logo、版本等打包信息 - https://uniapp.dcloud.io/collocation/manifest
pages.json - 配置页面路由、导航条、选项卡等页面类信息 - https://uniapp.dcloud.io/collocation/pages
uni.scss - 常量样式配置文件
```

#### Tips

* 编译到任意平台时 , `static`目录下的文件均会被打包进去 , 非`static`目录下的文件\(vue、js、css 等\)被引用到才会被包含进去
* `static`目录下的`js`文件不会被编译 , 如果里面有`es6`的代码 , 不经过转换直接运行 , 在手机设备上会报错
* `css`、`less/scss`等资源同样不要放在`static`目录下 , 建议这些公用的资源放在`common`目录下
* HbuilderX 1.9.0+ 支持在根目录创建`ext.json,sitemap.json`文件

| 有效目录 | 说明 |
| :--- | :--- |
| app-plus | App |
| h5 | H5 |
| mp-weixin | 微信小程序 |
| mp-alipay | 支付宝小程序 |
| mp-baidu | 百度小程序 |

  




