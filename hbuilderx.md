# HBuilderX

HBuilderX开发工具 - [https://www.dcloud.io/hbuilderx.html](https://www.dcloud.io/hbuilderx.html)

新建项目 - Command+N

默认选项即可创建 , 选择默认的配置 . 生成基础的模板 , 先看一下pages/index/index.vue :

```
<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
	</view>
</template>
```

常用的Vue标签 , 还有{{title}}表达式 , 用来绑定数据 . 再看script部分 :

```
<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>
```

其中data\(\)就是常用的model类 , 用来处理数据 .

编辑器工具栏中可以选择运行 , 也可以选择快捷按钮或快捷键Command+R选择运行环境 , 预览程序 .

在Mac系统中 , 选择偏好设置 , 打开Settings.json文件进行配置 . 其中运行配置可以设置一些真机调试的配置 .