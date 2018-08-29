<template>
  <div class="wrap">
    <div class="toubu"></div>
    <div class="zuo">
      <router-link to="/geren"><img src="/static/img/zuo.png" alt=""></router-link>
    </div>
    <p class="p1">身份实名认证</p>
    <router-link to="/shiming1"><p class="p2">添加新身份</p></router-link>
    <div class="tj">
      <div class="pink"></div>
     <div class="sf">
       暂无身份信息，请添加
     </div>
      <div class="hy">
        <div class="tjx">
          <router-link to="/shiming1"><p>添加新身份信息</p></router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Shiming"
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
    left: 25rem;
    top: 3rem;
  }
  .p2{
    position: absolute;
    font-size: 3rem;
    color: white;
    left: 55rem;
    top: 3.5rem;
  }
   .tj{
     position: absolute;
     width: 34.3rem;
     height: 44.1rem;
     /*border: 1px solid red;*/
     top: 18rem;
     left: 18rem;
   }
  .pink{
  position: absolute;
    width: 34.3rem;
    height: 31.1rem;
    background-color: rgb(254,227,227);
  }
  .sf{
    position: absolute;
    top: 32rem;
    left: 5rem;
    font-size: 2.4rem;
    color: rgb(128,128,128);
  }
  .hy{
    position: absolute;
    width:30rem;
    height: 6rem;
    border: 2px solid rgb(77,77,77);
    background-color:rgb(255,255,255);
    border-radius: 25rem;
    top: 38rem;
    left: 2rem;
  }
  .tjx{
    position: absolute;
    font-size: 3rem;
    color:rgb(77,77,77) ;
    left:5rem;
    top: 1rem;
  }
</style>
