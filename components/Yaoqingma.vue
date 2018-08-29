<template>
 <div class="wrap">
   <div class="toubu">
     <div class="zuo">
       <router-link to="/grxx"><img src="/static/img/zuo.png" alt=""></router-link>
     </div>
     <p class="p1">我的邀请码</p>
     <div class="nav"></div>
     <p class="nc">昵称</p>
     <p class="my">我的邀请码：1234567890</p>
     <button class="btn">分享邀请码  邀请好友注册吧</button>
 </div>
   </div>
</template>

<script>
    export default {
        name: "Yaoqingma"
    }
</script>

<style scoped>
  *{
    margin: 0;
    padding: 0;
  }
  .wrap{
    width:100%;
    background-color: rgb(242,242,242);
  }
  .toubu{
    width: 100%;
    height: 9.6rem;
    line-height: 9.6rem;
    background-color: rgb(229,62,66);
    position: relative;
  }
  .zuo img{
    position: absolute;
    left:3rem;
    top: 3rem;
    width: 2.3rem;
    height: 3.8rem;
  }
  .p1{
    font-size: 3.6rem;
    color: white;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%);
  }
  .nav{
    position: absolute;
    width: 10rem;
    height: 10rem;
    background-color: rgb(227,142,142);
    border-radius: 25rem;
    top: 15rem;
    left: 2rem;
  }
  .nc{
    position: absolute;
    font-size:3rem;
    top:16rem;
    left: 14rem;
  }
  .my{
    position: absolute;
    font-size: 3rem;
    top: 30rem;
    left: 18rem;
  }
  .btn{
    position: absolute;
    width: 52rem;
    height: 6rem;
    background-color: rgb(229,62,66);
    border-radius: 25rem;
    top: 42rem;
    font-size: 2.8rem;
    left: 10rem;
    color: white;
  }
</style>
