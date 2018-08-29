<template>
 <div class="wrap">
   <div class="toubu"></div>
   <div class="zuo">
     <router-link to="/qingchu"><img src="/static/img/zuo.png" alt=""></router-link>
   </div>
   <p class="p1">账户管理</p>
   <div class="zhh">
     <div class="ph">
       <img src="/static/img/shouji.png" alt="">
     </div>
     <div class="tel">
       手机号 :  15012340809
     </div>
   </div>
 </div>
</template>

<script>
    export default {
        name: "Zz"
    }
</script>

<style scoped>
  .wrap{
    margin: 0;
    padding: 0;
    width:72rem;
    height: 128rem;
    background-color:rgb(242,242,242) ;
    position: relative;
  }
  .toubu{
    position: absolute;
    border: 1px solid rgb(229,62,66);
    width: 72rem;
    height: 9.6rem;
    background-color: rgb(229,62,66);
  }
  .zuo img{
    position: absolute;
    left:3rem;
    top: 3rem;
    width: 2.3rem;
    height: 3.8rem;
  }
  .p1{
    position: absolute;
    font-size: 3.6rem;
    color: white;
    left: 28rem;
    top: 3rem;
  }
  .zhh{
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color: white;
    top: 10rem;
  }
  .ph img{
    position: absolute;
    width: 2.2rem;
    height: 3rem;
    top: 3rem;
    left: 2rem;
  }
  .tel{
    position: absolute;
    font-size: 2.8rem;
    top: 2.5rem;
    left: 6rem;
  }
</style>
