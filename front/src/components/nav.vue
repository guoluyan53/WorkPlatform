<template>
  <div class="nav">
    <ul class="ul">
        <!-- <li v-for="(item,index) in arr" 
            :key="item"
            :class="{'isActive':isActive}"
            @click="click(index)"
        >{{item}}</li> -->
        <li @click="click(0)" :class="{'isActive':$route.name=='Index'}">Index</li>
        <li @click="click(1)" :class="{'isActive':$route.name=='Task'}">Task</li>
        <li @click="click(2)" :class="{'isActive':$route.name=='Login'}">Login</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Nav',
  data(){
      return{
        //   arr:['Index','Task','Login'],
      }
  },
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
.ul{
    margin: 0;
    text-align: right;
}
li{
    list-style: none;
    display: inline-block;
    margin-top: 1rem;
    color: white;
    font-size: 2rem;
    margin-right: 5rem;
    cursor: pointer;
    transition: 0.2s linear;
}
.ul>li:hover{
    color: #0006b2;
}
/* 选中样式 */
.isActive{
    color: #0006b2;
}
</style>
