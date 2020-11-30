# 目录结构

```
componets/ - 组件,自定义组件目录
pages/ - 页面文件路由目录
    index/ - 默认首页
        index.vue
static/ - 静态文件目录
unpackage/ - 编译打包目录
    dist/
      dev/ - 测试目录
        app-plus - 手机端
        mp-weixin - 微信小程序
      build - 编译过后的目录
App.vue - 全局Vue文件
pages.json - 路由等页面相关配置文件
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



