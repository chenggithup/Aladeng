<template>
  <div class="wrap">
    <div class="toubu">
      <div class="zuo">
        <router-link to="/fankui"><img src="/static/img/zuo.png" alt=""></router-link>
      </div>
      <p class="p1">客服中心</p>
      <p class="p2">人工服务</p>
    </div>
    <div class="tb">
      <p class="time">10:30</p>
      <p class="jq">机器人为您服务</p>
    </div>
    <div class="music">
      <img src="/static/img/110.png" alt="">
    </div>
    <div v-if="bol" class="srk">
      <p class="t1">您好，我是机器人小灯。请问有什么可以
        帮助您的？机器人仅做引导，不处理或承
        诺任何售后问题。取消、退货等业务请务</p>
      <p class="t2">
        必找人工客服。多谢配合~</p>
    </div>
    <div class="huifu" v-show="bol2">
      <img src="/static/img/zh.png" alt="">
      <p class="pp"></p>
    </div>
    <div class="ll">
      <input type="text" value="" class="inp">
    </div>
    <div class="h1">

    </div>
    <button @click="fasong()" class="btn">发送</button>
  </div>
</template>

<script>
  export default {
    name: "Kefu",
    data() {
      return {
        bol: false,
        bol2:false
      }
    },
    methods: {
      fasong(){
        this.bol2=true;
        var va = $('.inp').val();
        $('.pp').html(va);
        $('.inp').val('');
      }
    },
    mounted: function () {
      setTimeout(() => {
        this.bol = true;
      }, 1000);
    }
  }
</script>

<style scoped>
  *{
    margin: 0;
    padding: 0;
  }
  .wrap{
    width:100%;
    background-color: #f2f2f2;
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
  .p2{
    position: absolute;
    font-size: 3rem;
    color: white;
    left: 58rem;
    top: 1rem;
  }
  .time{
    position: absolute;
    font-size: 2.4rem;
    color: #666666;
    top: 11rem;
    left: 32rem;
  }
  .jq{
    position: absolute;
    font-size: 3rem;
    color:rgb(128,128,128);
    top: 15rem;
    left: 25rem;
    background-color:rgb(230,230,230) ;
  }
  .music img{
    position: absolute;
    width: 8rem;
    height: 8rem;
    top: 23rem;
    left: 1.5rem;
  }
  .srk{
    position: absolute;
    width: 55rem;
    height: 20rem;
    background-color:rgb(223,233,239);
    top: 27rem;
    left: 12rem;
  }
  .t1{
    position: absolute;
    font-size: 2.8rem;
    left: 1.5rem;
    top: 1rem;
  }
  .t2{
    position: absolute;
    font-size: 2.8rem;
    top: 13rem;
    left: 3rem;
  }
  .ll input{
    position: fixed;
    width: 58rem;
    height: 8rem;
    background-color: #fff;
    bottom: 0;
    left: 0;
    font-size: 2.8rem;
    margin-left: 2rem;
  }
  .h1{
    position: absolute;
    width: 58rem;
    height: 0.2rem;
    background-color: rgb(204,204,204);
    top: 126rem;
    left: 2rem;
  }
  .btn{
    position: absolute;
    width:8rem;
    height: 4rem;
    background-color: rgb(223,233,239);
    font-size:2.8rem;
    color: rgb(97,167,234);
    top: 123rem;
    left: 62rem;
  }
  .huifu{
    width: 100%;
    text-align: left;
  }
  .huifu img{
    width: 8rem;
    height: 8rem;
    position: absolute;
    right: 2rem;
    top: 60rem;
  }
  .pp{
    font-size:2.8rem;
    color: rgb(97,167,234);
    position: absolute;
    right: 12rem;
    margin-left: 5rem;
    top: 62rem;
    background-color: #0f0;
  }
</style>
