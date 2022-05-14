> 记录一下遇到的问题以及解决方案。

## 1.导航栏切换样式不改变的问题

导航栏切换的样式改变这里使用了 `$route.name`来判断是否是当前页面，这样做即使刷新了样式也不会消失。

**注意选择器的优先级问题！！！**

下面只列出了关键代码：

```vue
<template>
  <div class="nav">
    <ul class="ul">
        <li @click="click(0)" :class="{'isActive':$route.name=='Index'}">Index</li>
        <li @click="click(1)" :class="{'isActive':$route.name=='Task'}">Task</li>
        <li @click="click(2)" :class="{'isActive':$route.name=='Login'}">Login</li>
    </ul>
  </div>
</template>

<script>
export default {
  methods:{
      click(e){
          if(e==0){
              this.$router.push('/');
          }else if(e==1){
              this.$router.push('/task');
          }else if(e==2){
              this.$router.push('/login')
          }
      }
  }
}
</script>

<style scoped>
/*
原来是这么写的，但是样式并没有改变！！注意优先级！！
.ul>li{
         color: white;
}*/
li{
    color: white;
}
/* 选中样式 */
.isActive{
    color: #0006b2;
}
</style>

```

