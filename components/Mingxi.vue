<template>
    <div class="wrap">
      <div class="toubu"></div>
      <div class="zuo">
        <router-link to="/shz"><img src="/static/img/zuo.png" alt=""></router-link>
      </div>
      <p class="p1">神灯值明细</p>
      <div class="one">
        <router-link to="/yaoqingma"><p class="pp1">邀请一位好友注册 (18712340809)</p></router-link>
        <div class="day">
          2017-08-10
        </div>
        <div class="ten">
          +10
        </div>
      </div>
      <div class="one1">
        <router-link to="/yaoqingma"><p class="pp1">邀请一位好友注册 (18712340809)</p></router-link>
        <div class="day1">
          2017-08-10
        </div>
        <div class="ten1">
          +10
        </div>
    </div>
    </div>
</template>

<script>
    export default {
        name: "Mingxi"
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
  .one{
    position: absolute;
    background-color:rgb(255,255,255);
    border: 1px solid rgb(204,204,204);
    width: 72rem;
    height: 10rem;
    top: 9.5rem;
  }
  .pp1{
    position: absolute;
    font-size: 2.4rem;
    top: 3rem;
    left: 2rem;
  }
  .day{
    position: absolute;
    font-size:2rem;
    top: 6rem;
    left: 2rem;
  }
  .ten{
    position: absolute;
    font-size: 3.6rem;
    color: rgb(229,62,66);
    left: 62rem;
    top: 3rem ;
  }
  .one1{
    position: absolute;
    background-color:rgb(255,255,255);
    border: 1px solid rgb(204,204,204);
    width: 72rem;
    height: 10rem;
    top: 19rem;
  }
  .pp01{
    position: absolute;
    font-size: 2.4rem;
    top: 3rem;
    left: 2rem;
  }
  .day1{
    position: absolute;
    font-size:2rem;
    top: 6rem;
    left: 2rem;
  }
  .ten1{
    position: absolute;
    font-size: 3.6rem;
    color: rgb(229,62,66);
    left: 62rem;
    top: 3rem ;
  }
</style>
