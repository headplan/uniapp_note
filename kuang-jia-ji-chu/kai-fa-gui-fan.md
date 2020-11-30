# 开发规范

为了实现多端兼容 , 综合考虑编译速度、运行性能等因素 , `uni-app`约定了如下开发规范 : 

* 页面文件遵循\[ Vue单文件组件\(SFC\)规范 \] - https://vue-loader.vuejs.org/zh/spec.html
* 组件标签靠近小程序规范 \[uni-app组件规范\] - https://uniapp.dcloud.io/component/README
* 接口能力\(JS API\)靠近微信小程序规范 , 但需将前缀`wx`替换为`uni`\[uni-app接口规范\] - https://uniapp.dcloud.io/api/README
* 数据绑定及事件处理同`Vue.js`规范 , 同时补充了App及页面的生命周期 . 
* 为兼容多端运行，建议使用flex布局进行开发



