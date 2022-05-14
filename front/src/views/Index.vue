<template>
    <div class="index">
        <header class="header">
            <Nav></Nav>
        </header>
        <div class="content">
            <h2>Submit your</h2>
            <h2>homework</h2>
            <h2>now</h2>
            <p>Your work will be graded and evaluated after</p>
            <p>submission,please pay attention to it in time</p>
            <p>hope you can submit a satisfactory answer sheet</p>
            <input type="button" value="Let us start" class="btn">
        </div>
    </div>
</template>

<script>
import Nav from "../components/nav.vue";
export default {
  name: 'Index',
  components:{
      Nav
  },
  data(){
      return{

      }
  }
}
</script>

<style scoped>
.index{
    position: relative;
    width: 100%;
    height: 100vh;
    background: url("../assets/image/index.png");
    background-size: 100% 100%;
}
.content{
    position: absolute;
    left: 5rem;
    top: 8rem;
    text-align: left;
}
.content h2{
    color: #2f5ee8;
    font-size: 3rem;
    margin: 0.2rem;
}
.content p{
    color: #8993b1;
    font: 1rem;
    margin: 0.1rem;
}
.btn{
    margin-top: 1rem;
    width: 10rem;
    height: 2rem;
    border-radius: 20px;
    color: white;
    font-size: 1rem;
    border: none;
    background-color:#2f5ee8;
    cursor: pointer;
}
</style>