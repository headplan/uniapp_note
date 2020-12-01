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



