# 框架基础

* MVC与MVVM思想
* 项目结构与文件类型
* 全局标题与页面标题
* 全局样式与页面样式
* App的声明周期
* 页面的声明周期
* 数据绑定与事件
* 组件中的动态与静态变量\(表达式\)
* 条件判断与for循环
* 多端兼容条件编译

#### MVC

M - model模型层 , 数据的增删改查

V - view视图层 , 前端页面\(html/js/css\)

C - contoller控制层 , 处理业务逻辑

#### MVVM

MVVM是Model-View-ViewModel的简写 . 它本质上就是MVC 的改进版 . MVVM 就是将其中的View的状态和行为抽象化 , 让我们将视图 UI 和业务逻辑分开 . 当然这些事 ViewModel 已经帮我们做了 , 它可以取出 Model 的数据同时帮忙处理 View 中由于需要展示内容而涉及的业务逻辑 .

M - mode单页面的静态数据

VM - viewmodel核心调度者协调器

V - 页面HTML

通过VM数据双向绑定 .

#### 代码示例

* template标签中是html代码 , 代表一个页面 , 这里的view和html中的div一样 . V
* script标签中是JS代码 . VM
* style样式代码 . 

上面的三个标签在每个页面都只能存在一个 . 

```
<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
			<input type="text" :value="title" @input="change" />
		</view>
		<view>
			I am {{student.age}} years old.<br/>
			I have skills such as: {{skill[0]}},{{skill[1]}},{{skill[2]}},{{skill[3]}},{{skill[4]}}
		</view>
	</view>
</template>
```

```
<script>
	export default {
		data() {
			return {
				title: 'HelloWorld',
				student: {
					age: 18,
				},
				skill: ['Java', 'HTML', 'CSS', 'SpringCloud', 'VUE']
			}
		},
		onLoad() {

		},
		methods: {
			change(e) {
				var titleTxt = e.detail.value;
				this.title = titleTxt;
				// debugger;
			}
		}
	}
</script>
```

```
<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
```



