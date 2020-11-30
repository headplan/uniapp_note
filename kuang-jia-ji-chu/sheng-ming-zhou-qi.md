# 生命周期

#### 应用生命周期

`uni-app`支持如下应用生命周期函数 : 

| 函数名 | 说明 |
| :--- | :--- |
| onLaunch | 当`uni-app`初始化完成时触发\(全局只触发一次\) |
| onShow | 当`uni-app`启动 , 或从后台进入前台显示 |
| onHide | 当`uni-app`从前台进入后台 |
| onError | 当`uni-app`报错时触发 |
| onUniNViewMessage | 对`nvue`页面发送的数据进行监听 , 可参考https://uniapp.dcloud.io/use-weex?id=nvue-向-vue-通讯 |
| onUnhandledRejection | 对未处理的 Promise 拒绝事件监听函数（2.8.1+） |
| onPageNotFound | 页面不存在监听函数 |
| onThemeChange | 监听系统主题变化 |



