# 生命周期

#### 应用生命周期

`uni-app`支持如下应用生命周期函数 :

| 函数名 | 说明 |
| :--- | :--- |
| onLaunch | 当`uni-app`初始化完成时触发\(全局只触发一次\) |
| onShow | 当`uni-app`启动 , 或从后台进入前台显示 |
| onHide | 当`uni-app`从前台进入后台 |
| onError | 当`uni-app`报错时触发 |
| onUniNViewMessage | 对`nvue`页面发送的数据进行监听 , 可参考[https://uniapp.dcloud.io/use-weex?id=nvue-向-vue-通讯](https://uniapp.dcloud.io/use-weex?id=nvue-向-vue-通讯) |
| onUnhandledRejection | 对未处理的 Promise 拒绝事件监听函数（2.8.1+） |
| onPageNotFound | 页面不存在监听函数 |
| onThemeChange | 监听系统主题变化 |

#### 注意

* 应用生命周期仅可在`App.vue`中监听 , 在其它页面监听无效
* onlaunch里进行页面跳转 , 如遇白屏报错请参考[https://ask.dcloud.net.cn/article/35942](https://ask.dcloud.net.cn/article/35942)

#### 页面声明周期

`uni-app`支持如下页面生命周期函数 :

| 函数名 | 说明 | 平台差异说明 | 最低版本 |
| :--- | :--- | :--- | :--- |
| onLoad | 监听页面加载 , 其参数为上个页面传递的数据 , 参数类型为Object\(用于页面传参\) , 参考[https://uniapp.dcloud.io/api/router?id=navigateto](https://uniapp.dcloud.io/api/router?id=navigateto) |  |  |
| onShow | 监听页面显示 . 页面每次出现在屏幕上都触发 , 包括从下级页面点返回露出当前页面 |  |  |
| onReady | 监听页面初次渲染完成 . 注意如果渲染速度快 , 会在页面进入动画完成前触发 |  |  |
| onHide | 监听页面隐藏 |  |  |
| onUnload | 监听页面卸载 |  |  |
| onResize | 监听窗口尺寸变化 | App、微信小程序 |  |
| onPullDownRefresh | 监听用户下拉动作 , 一般用于下拉刷新 , 参考https://uniapp.dcloud.io/api/ui/pulldown |  |  |
| onReachBottom | 页面上拉触底事件的处理函数 |  |  |
| onTabItemTap | 点击 tab 时触发 , 参数为Object , 具体见下方注意事项 | 微信小程序、百度小程序、H5、App（自定义组件模式） |  |
| onShareAppMessage | 用户点击右上角分享 | 微信小程序、百度小程序、字节跳动小程序、支付宝小程序 |  |
| onPageScroll | 监听页面滚动 , 参数为Object |  |  |
| onNavigationBarButtonTap | 监听原生标题栏按钮点击事件，参数为Object | 5+ App、H5 |  |
| onBackPress | 监听页面返回，返回 event = {from:backbutton、 navigateBack} ，backbutton 表示来源是左上角返回按钮或 android 返回键；navigateBack表示来源是 uni.navigateBack ；详细说明及使用：[onBackPress 详解](http://ask.dcloud.net.cn/article/35120) | App、H5 |  |
| onNavigationBarSearchInputChanged | 监听原生标题栏搜索输入框输入内容变化事件 | App、H5 | 1.6.0 |
| onNavigationBarSearchInputConfirmed | 监听原生标题栏搜索输入框搜索事件，用户点击软键盘上的“搜索”按钮时触发。 | App、H5 | 1.6.0 |
| onNavigationBarSearchInputClicked | 监听原生标题栏搜索输入框点击事件 | App、H5 | 1.6.0 |
| onShareTimeline | 监听用户点击右上角转发到朋友圈 | 微信小程序 | 2.8.1+ |
| onAddToFavorites | 监听用户点击右上角收藏 | 微信小程序 | 2.8.1+ |



