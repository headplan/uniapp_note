# 目录结构

```
componets/ - 组件,自定义组件目录
pages/ - 页面文件路由目录
    index/ - 默认首页
        index.vue
pages.json - 路由配置文件
```

#### pages.json

路由配置项 - https://uniapp.dcloud.io/collocation/pages

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



