# cloudfunctions

uniCloud是DCloud联合阿里云 , 腾讯云为开发者提供的基于serverless模式和js编程的源开发平台 .

`uniCloud`的 web控制台地址 :  [https://unicloud.dcloud.net.cn](https://unicloud.dcloud.net.cn/)

#### uniCloud的价值

对于程序员 , 从此你又get一个新技能 , 用熟悉的js , 轻松搞定前后台整体业务 .

对于开发商 :

* 减少开发成本 . 
* 专注业务 , 不再操心服务器运维 . 
* 不发布H5版 , 不需要购买备案域名 , 小程序和App可以免域名使用 . 
* 敏捷性业务可以按照业务分工 , 不再按照前后端分工 . 

#### uniCloud的运行原理

**开发和运行流程**

* 开发者在HBuilderX里为项目新建 uniCloud 云环境\(可选择阿里云或腾讯云\) , 在云函数目录下编写js代码 , 上传部署云函数到阿里云或腾讯云的 serverless 环境中 . 
* 前端代码通过`uniCloud.callFunction()`方法调用云函数 . 
* 云函数中可执行js运算、读写云化数据库（NoSQL）、读写存储和CDN、操作网络 , 给前端返回数据 . 

开发过程 , 连接DCloud服务器 ; 运行过程是手机端直连阿里云或腾讯云 serverless 环境 , 不通过DCloud服务器中转 .

uniCloud 的底层环境 , 和微信小程序云开发、支付宝小程序云开发的基建环境相同 . 功能、性能、稳定性有足够的保障 . 腾讯云云开发\(CloudBase\)提供基础 serverless 能力 , 微信团队基于该能力封装了微信云开发 , 而DCloud团队基于该能力封装了 uniCloud . 阿里云类似 .

**uniCloud 基建部分主要包括如下3部分**

* 云函数 - 在云端运行的js代码 . 运行在定制过的node环境中 , 有良好的性能和强大的功能 . serverless环境无需自行加购服务器处理增容 , 云函数按量付费 , 不管多大的并发都扛得住\(阿里云serverless已经经过了双11的考验\)
* 数据库 - 可在云函数中读写的、基于 NoSQL 的 JSON 数据库 . 这种数据库对于前端工程师更自然 , 不需要学习SQL、不需要理解关系型和设计主键 . 
* 存储和CDN - 不管在前端还是云函数中 , 都可以操作存储和CDN . 在
  `uniCloud`提供的安全机制下 , 可以实现应用前端直传CDN , 避免服务器中转的耗时和带宽占用 , 且不会发生盗传 . 

#### serverless和云的发展趋势

serverless是目前很火的概念 , 它是下一代云技术 , 是真正的“云” . 下一代基于serverless的云 , 真正的把计算、存储的能力进行了云化 , 开发者只需要按量租用这些计算和存储能力 , 再也不用买虚拟机 , 自己装服务器了 . 

广义的serverless , 是泛语言的，PHP、JAVA、Node.js都可以用 serverless . 但基于 js 的 serverless , 更被业内所看中 . 

在 serverless 成熟后 , 紧接着出现了小程序云开发 . 微信、支付宝、百度都上线了自己的云开发 , 以帮助开发者云端一体的完成业务 . 根据微信公开的数据 , 已经有50万开发者在使用微信云开发了 . 



