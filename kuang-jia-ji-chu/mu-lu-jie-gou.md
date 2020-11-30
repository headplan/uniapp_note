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
App.vue - 应用配置,用来配置App全局样式以及监听
main.js - Vue初始化入口文件
manifest.json - 配置应用名称、appid、logo、版本等打包信息
pages.json - 配置页面路由、导航条、选项卡等页面类信息
uni.scss - 常量样式配置文件
```

#### pages.json

详细可以查看pages.json配置

路由配置项 - [https://uniapp.dcloud.io/collocation/pages](https://uniapp.dcloud.io/collocation/pages)

```
{
    "pages": [ //pages数组中第一项表示应用启动页，参考：https://uniapp.dcloud.io/collocation/pages
        {
            "path": "pages/index/index",
            "style": {
                "navigationBarTitleText": "uni-app"
            }
        }
    ],
    "globalStyle": {
        "navigationBarTextStyle": "black",
        "navigationBarTitleText": "uni-app",
        "navigationBarBackgroundColor": "#F8F8F8",
        "backgroundColor": "#F8F8F8"
    }
}
```



