# HBuilderX

HBuilderX开发工具 - [https://www.dcloud.io/hbuilderx.html](https://www.dcloud.io/hbuilderx.html)

新建项目 - Command+N

默认选项即可创建 , 选择默认的配置 . 生成基础的模板 , 先看一下pages/index/index.vue : 

```
<template>
	<text class="title">{{title}}</text>
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

其中`data()`就是常用的model类 , 用来处理数据 . 

编辑器工具栏中可以选择运行 , 也可以选择快捷按钮或快捷键Command+R选择运行环境 , 预览程序 . 





