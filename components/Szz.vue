<template>
  <div class="wrap">
    <div class="toubu"></div>
    <div class="zuo">
      <img src="/static/img/zuo.png" alt="">
    </div>
    <p class="p1">设置</p>
    <div class="cc">
      <ul>
        <li>账户管理</li>
      </ul>
      <div class="rig">
        <img src="/static/img/you.png" alt="">
      </div>
    </div>
    <div class="dd">
      <div class="password">
        <ul>
          <li>修改登录密码</li>
        </ul>
      </div>
      <div class="right">
        <img src="/static/img/you.png" alt="">
      </div>
    </div>
    <div class="f1">
      <div class="cle">
        清除缓存
      </div>
      <div class="byte">
        10KB
      </div>
    </div>
    <div class="cc1">
      <ul>
        <li>阿拉灯平台用户协议</li>
      </ul>
      <div class="rig1">
        <img src="/static/img/you.png" alt="">
      </div>
    </div>
    <div class="dd1">
      <div class="password1">
        <ul>
          <li>个人委托协议</li>
        </ul>
      </div>
      <div class="right1">
        <img src="/static/img/you.png" alt="">
      </div>
    </div>
    <div class="f11">
      <div class="cle1">
        检查更新
      </div>
      <div class="skt">
        <img src="/static/img/you.png" alt="">
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    name: "Shezhi"
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
  .cc{
    position: absolute;
    width: 72rem;
    height: 10rem;
    border: 1px solid grey;
    background-color: white;
    top: 11rem;
  }
  .cc ul li{
    position: absolute;
    font-size: 2.8rem;
    left: 2rem;
    top: 4rem;
  }

  .rig img{
    position: absolute;
    width: 1rem;
    height: 1.8rem;
    top: 4rem;
    left: 70rem;
  }
  .dd{
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color: white;
    border: 1px solid rgb(204,204,204);
    top: 21rem;
  }
  .password ul li{
    position: absolute;
    font-size: 2.8rem;
    top: 3rem;
    left: 2rem;
  }
  .right img{
    position: absolute;
    width: 1rem;
    height: 1.8rem;
    left: 70rem;
    top: 4rem;
  }
  .f1{
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color: white;
    top:31.2rem;
  }
  .cle{
    position: absolute;
    font-size: 2.8rem;
    top: 3rem;
    left: 2rem;
  }
  .byte{
    position: absolute;
    font-size: 2.4rem;
    top: 3rem;
    left: 63rem;
  }
  .cc1{
    position: absolute;
    width: 72rem;
    height: 10rem;
    /*border: 1px solid grey;*/
    background-color: white;
    top: 41.4rem;
  }
  .cc1 ul li{
    position: absolute;
    font-size: 2.8rem;
    left: 2rem;
    top: 3rem;
  }

  .rig1 img{
    position: absolute;
    width: 1rem;
    height: 1.8rem;
    top: 4rem;
    left: 70rem;
  }
  .dd1{
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color: white;
    border: 1px solid rgb(204,204,204);
    top: 51rem;
  }
  .password1 ul li{
    position: absolute;
    font-size: 2.8rem;
    top: 3rem;
    left: 2rem;
  }
  .right1 img{
    position: absolute;
    width: 1rem;
    height: 1.8rem;
    left: 70rem;
    top: 4rem;
  }
  .f11{
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color: white;
    top:61.3rem;
  }
  .cle1{
    position: absolute;
    font-size: 2.8rem;
    top: 3rem;
    left: 2rem;
  }
  .skt img{
    position: absolute;
    width: 1rem;
    height: 1.8rem;
    top: 4rem;
    left: 70rem;
  }
  .slider{
    position: absolute;
    border: 1px solid rgb(204,204,204);
    background-color: gray;
    width:20rem;
    height: 6rem;
    top: 75rem;
    left: 25rem;
  }
  .jx{
    position: absolute;
    font-size: 3rem;
    color: white;
    top: 1rem;
    left: 4.5rem;
  }
</style>
