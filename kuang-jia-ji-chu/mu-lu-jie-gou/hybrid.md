# hybrid目录

存放本地网页的目录 . 

#### web-view

`web-view`是一个 web 浏览器组件 , 可以用来承载网页的容器 , 会自动铺满整个页面\(nvue 使用需要手动指定宽高\) . 

> 各小程序平台 , web-view加载的url需要在后台配置域名白名单 , 包括内部再次iframe内嵌的其他url .

**属性说明**

| 属性名 | 类型 | 说明 | 平台差异说明 |
| :--- | :--- | :--- | :--- |
| src | String | webview 指向网页的链接 |  |
| allow | String | 用于为[iframe](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe)指定其[特征策略](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/%E7%AD%96%E7%95%A5%E7%89%B9%E5%BE%81) | H5 |
| sandbox | String | 该属性对呈现在[iframe](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe)框架中的内容启用一些额外的限制条件。 | H5 |
| webview-styles | Object | webview 的样式 | App-vue |
| @message | EventHandler | 网页向应用`postMessage`时，会在特定时机（后退、组件销毁、分享）触发并收到消息。 | H5 暂不支持（可以直接使用[window.postMessage](https://developer.mozilla.org/zh-CN/docs/Web/API/Window/postMessage)） |
| @onPostMessage | EventHandler | 网页向应用实时`postMessage` | App-nvue |

**src**

| 来源 | App | H5 | 微信小程序 | 支付宝小程序 | 百度小程序 | 字节跳动小程序 | QQ小程序 | 快应用 | 360小程序 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 网络 | √ | √ | √ | √ | √ | √ | √ | √ | √ |
| 本地 | √ | √ | x | x | x | x | x | x | x |



