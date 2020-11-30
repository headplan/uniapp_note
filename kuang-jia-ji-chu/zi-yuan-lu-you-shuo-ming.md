# 资源路由说明

#### 模板内引入静态资源

`template`内引入静态资源 , 如`image`、`video`等标签的`src`属性时 , 可以使用相对路径或者绝对路径 , 形式如下 :

```
<!-- 绝对路径，/static指根目录下的static目录，在cli项目中/static指src目录下的static目录 -->
<image class="logo" src="/static/logo.png"></image>
<image class="logo" src="@/static/logo.png"></image>
<!-- 相对路径 -->
<image class="logo" src="../../static/logo.png"></image>
```

**注意**

* `@`开头的绝对路径以及相对路径会经过base64转换规则校验
* 引入的静态资源在非h5平台 , 均不转为base64
* H5平台 , 小于4kb的资源会被转换成base64 , 其余不转
* 自`HBuilderX 2.6.6-alpha`起`template`内支持`@`开头路径引入静态资源 , 旧版本不支持此方式
* App平台自`HBuilderX 2.6.9-alpha`起`template`节点中引用静态资源文件时 , 调整查找策略为\[ 基于当前文件的路径搜索 \] , 与其他平台保持一致
* 支付宝小程序组件内 image 标签不可使用相对路径

#### JS文件引入

`js`文件或`script`标签内\(包括renderjs等\)引入`js`文件时 , 可以使用相对路径和绝对路径 , 形式如下

```
// 绝对路径,@指向项目根目录,在cli项目中@指向src目录
import add from '@/common/add.js'
// 相对路径
import add from '../../common/add.js'
```

**注意**

* js文件不支持使用`/`开头的方式引入

#### CSS引入静态资源

`css`文件或`style标签`内引入`css`文件时\(scss、less文件同理\) , 可以使用相对路径或绝对路径`(HBuilderX 2.6.6-alpha)`

```
/* 绝对路径 */
@import url('/common/uni.css');
@import url('@/common/uni.css');
/* 相对路径 */
@import url('../../common/uni.css');
```

**注意**

自`HBuilderX 2.6.6-alpha`起支持绝对路径引入静态资源 , 旧版本不支持此方式 . 

> `css`文件或`style标签`内引用的图片路径可以使用相对路径也可以使用绝对路径 , 需要注意的是有些小程序端css文件不允许引用本地文件\(请看注意事项\)

```
/* 绝对路径 */
background-image: url(/static/logo.png);
background-image: url(@/static/logo.png);
/* 相对路径 */
background-image: url(../../static/logo.png);
```

**Tips**

* 引入字体图标请参考 , https://uniapp.dcloud.io/frame?id=字体图标
* `@`开头的绝对路径以及相对路径会经过base64转换规则校验
* 不支持本地图片的平台 , 小于40kb , 一定会转base64\(共四个平台mp-weixin, mp-qq, mp-toutiao, app v2\)
* h5平台 , 小于4kb会转base64 , 超出4kb时不转
* 其余平台不会转base64



