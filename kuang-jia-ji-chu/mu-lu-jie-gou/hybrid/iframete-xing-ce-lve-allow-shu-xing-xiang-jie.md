# iframe特性策略allow属性详解

allow属性的使用需要参考特性策略这一小节 . 特性策略可以允许你控制页面或者iframe可以使用哪些特性 . 页面控制的话设置在HTTP头部的Feature-Policy的这个字段 , iframe的话就是我们要说的这个allow字段 . 

**特性策略的书写规则**

```
<feature name> <allowlist of origin(s)>
```

**完整的特性名称参考**

```
Policy Controlled Features或者Feature-Policy
```

**而allowlist则有如下规则**

* \* - 表示该特性在该文档下都是允许的 , 包括所有的嵌套的浏览内容\(iframes\) , 而不用管这些内容的源
* self - 表示该特性在该文档下都是允许的 , 并且仅在同源的情况下嵌套的浏览内容\(iframes\)才可以使用
* src - \(iframes的allow属性专用\)表示该特性在这个iframe下允许使用 , 只要加载的文档来源的源和iframe的src属性指定的URL是同源的
* none - 表示该特性在顶层以及嵌套的浏览内容下都是被禁用的
* `<origin(s)>` - 表示该特性只在一些指定的源下才允许使用 , 多个源使用空格隔开

这里主要讲一下iframe下的allow属性 , 比如不允许iframe的页面全屏、不允许调用摄像头之类的行为 , 可以这么配置 : 

```
<iframe allow="camera 'none'; fullscreen 'none'">
```

比如只允许同源的才可以使用全屏这个特性 : 

```
<iframe src="https://example.com..." allow="fullscreen 'src'"></iframe>
```

比如只允许指定源才可以使用定位功能 : 

```
<iframe src="https://google-developers.appspot.com/demos/..." allow="geolocation https://google-developers.appspot.com"></iframe>
```

allow的值有 : 

* Accelerometer
* Ambient light sensor
* Autoplay
* Camera
* Encrypted media
* Fullscreen
* Geolocation
* Gyroscope
* Lazyload
* Microphone
* Midi
* PaymentRequest
* Picture-in-picture
* Speaker
* USB
* VR / XR

  


