<template>
  <div class="wrap">
    <div class="top">
      <router-link to="/geren"><img src="/static/img/fanhui.png" alt=""></router-link>
      <span>客服与反馈</span>
      <span style="margin-right: 2rem">反馈</span>
    </div>
    <div class="tishi">
      <span>安全提示:</span>
      <span>阿拉灯不会以付款异常、系统升级等原因让顾客进行银行账户修改。请勿相信陌生电话、短信内容,阿拉丁提醒您谨防诈骗</span>
    </div>
    <div class="one">
      <router-link to="/kefu"><span>联系客服</span></router-link><span>工作时间:</span> <span>9:00-24:00</span>
    </div>
    <div class="two">
      <img class="logo" src="/static/img/tubiao.png" alt="">
      <span class="xq">订单咨询</span>
      <span class="xg">订单修改、取消订单、订单查询</span>
      <img class="you" src="/static/img/youred.png" alt="">
    </div>

    <div class="two">
      <img class="logo" src="/static/img/tub02.png" alt="">
      <span class="xq">订单咨询</span>
      <span class="xg">订单修改、取消订单、订单查询</span>
      <img class="you" src="/static/img/youred.png" alt="">
    </div>

    <div class="two">
      <img class="logo" src="/static/img/tub03.png" alt="">
      <span class="xq">订单咨询</span>
      <span class="xg">订单修改、取消订单、订单查询</span>
      <img class="you" src="/static/img/youred.png" alt="">
    </div>

    <div class="wenti">
      <div><span>常见问题</span></div>
      <ul class="ul1">
        <li>
          <span>食品安全科普</span> <img src="/static/img/you.png" alt="">
        </li>
        <li>
          <span>为什么还没有发货?</span> <img src="/static/img/you.png" alt="">
        </li>
        <li>
          <span>发货了没有收到</span> <img src="/static/img/you.png" alt="">
        </li>
        <li>
          <span>其他问题</span> <img src="/static/img/you.png" alt="">
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Fankui"
  }
</script>

<style scoped>
  *{
    margin: 0;
    padding:0;}
  .wrap{
    width: 100%;background-color: #f2f2f2;
  }
  .top{display: flex;justify-content:space-between;background-color: red;
    height: 11.3rem;
    width: 100%;

  }
  .top img:nth-child(1){
    width: 2.3rem;
    height: 3.8rem;
    margin-top:3.7rem;
    margin-left: 2rem;
  }

  .top span{font-size: 3.6rem;margin-top: 3.7rem;color: white;}
  .tishi{
    width: 100%;
    height: 13rem;
    background-color: #f9d3d4;
    text-align: left;
    padding-left: 1rem;
  }
  .tishi span:nth-child(1){
    font-size: 2.8rem;
    color: red;
  }
  .tishi span:nth-child(2){
    font-size: 2.5rem;
    color:  #4d4d4d;

  }
  .one{
    width: 100%;
    height: 4rem;
    margin-top: 1rem;
    position: relative;
  }
  .one span{
    font-size: 2rem;
    color: #4d4d4d;
    position: absolute;
  }
  .one span:nth-child(1){

    left: 3rem;
  }
  .one span:nth-child(2){
    right: 14rem;
  }
  .one span:nth-child(3){
    color: red;
    top: 0.3rem;
    right: 3rem;
  }
  .two{
    width: 68rem;
    height: 14rem;
    background-color: #ffffff;
    border-radius: 2px;
    border: solid 1px #cccccc;
    margin-left: 2rem;
    position: relative;
    margin-top: 2rem;
  }
  .logo{
    width: 8rem;
    height: 8rem;
    margin-left: -55rem;
    margin-top: 2rem;
  }
  .xq{
    font-size: 2.8rem;
    position: absolute;
    left: 12rem;
    top:2rem;
  }
  .xg{
    font-size: 2rem;
    position: absolute;
    left: 12rem;
    color: #808080;
    top:8rem;
  }
  .you{
    position: absolute;
    right: 2rem;
    width: 1.4rem;
    height: 2.4rem;
    top: 6rem;
  }
  .wenti{
    margin-top: 2rem;
    background-color: white;

  }
  .wenti div{
    width: 100%;
    background-color: #f2f2f2;
    text-align: left;
  }
  .wenti div span{
    font-size: 2.8rem;
    margin-left: 2rem;

  }
  .ul1 li{
    width: 100%;
    height: 6rem;
    border-bottom: 1px #cccccc solid;
    line-height: 6rem;
    position: relative;
    text-align: left;

  }
  .ul1 li span{
    font-size: 2.8rem;
    margin-left: 2rem;
  }
  .ul1 li img{
    width: 1.4rem;
    height: 2.4rem;
    position: absolute;
    right: 2rem;
    top:2rem;
  }


</style>
