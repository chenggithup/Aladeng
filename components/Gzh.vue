<template>
    <div class="wrap">
      <div class="toubu"></div>
      <div class="zuo">
        <router-link to="/geren"><img src="/static/img/zuo.png" alt=""></router-link>
      </div>
      <p class="p1">关注公众号</p>
      <div class="fw">
        微信服务号 :
      </div>
      <div class="as">
        aladeng
      </div>
      <div class="save">
        长按可复制
      </div>
      <div class="sma">
        <img src="/static/img/fangzi.png" alt="">
      </div>
      <div class="ma">
        <img src="/static/img/masaike.png" alt="">
      </div>
      <div class="sao">
        您可以：通过微信”扫一扫”扫描上方二维码，找到我们
      </div>
      <div class="ll"></div>
        <div class="Wx">
             关注阿拉灯微信服务号
        </div>
        <div class="wl">
          发货、物流、补货
        </div>
        <div class="now">
          通知早知道
        </div>
    </div>

</template>

<script>
    export default {
        name: "Gzh"
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
  .fw{
    position: absolute;
    font-size: 2.8rem;
    top: 15rem;
    left: 30rem;
  }
  .as{
    position: absolute;
    font-size:2.8rem;
    color: rgb(229,62,66);
    top: 19.5rem;
    left: 32rem;
  }
  .save{
    position: absolute;
    font-size: 2.4rem;
    color: #666666;
    top: 24rem;
    left: 31rem;
  }
  .sma img{
    position: absolute;
    width: 100rem;
    height:95rem;
    top: 10rem;
    left: -10rem;
  }
  .ma img{
    position: absolute;
    width:20.4rem;
    height: 20.4rem;
    top: 50rem;
    left: 29rem;
  }
  .sao{
    position: absolute;
    font-size: 2.4rem;
    top: 90rem;
    left: 8rem;
  }
  .ll{
    position: absolute;
    width: 60rem;
    height: 0.2rem;
    background-color:rgb(204,204,204);
    top: 97rem;
    left: 6rem;
  }
  .Wx{
    position: absolute;
    font-size: 2.4rem;
    left: 24rem;
    top: 103rem;
  }
  .wl{
    position: absolute;
    font-size: 2.8rem;
    top: 107rem;
    left: 19rem;
  }
  .now{
    position: absolute;
    font-size: 2.4rem;
    top: 107.5rem;
    left: 41.5rem;
  }
</style>
