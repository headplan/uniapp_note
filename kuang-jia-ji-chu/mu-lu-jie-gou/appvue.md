# App.vue

```
<script>
    export default {
        onLaunch: function() {
            console.log('App Launch')
        },
        onShow: function() {
            console.log('App Show')
        },
        onHide: function() {
            console.log('App Hide')
        }
    }
</script>

<style>
    /*每个页面公共css */
</style>
```

全局脚本 , 全局样式文件 .

响应的每个页面也可以覆盖全局的属性 . 

