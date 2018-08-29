<template>
  <div class="wrap">
    <div class="toubu">
      <router-link to="/geren"><img src="/static/img/zuo.png" alt=""></router-link>
      <p class="p1">个人信息</p>
    </div>

    <div class="center">
      <ul class="ul1">
        <li>
          <span>头像</span>
          <div class="span1">
            <p>头像</p>
            <p>图片</p>
          </div>
          <router-link to="/touxiang"><img src="/static/img/you.png" alt=""></router-link>
        </li>
        <li>
          <span>昵称</span>
          <span>夏至未至</span>
          <router-link to="/name"><img src="/static/img/you.png" alt=""></router-link>
        </li>
        <li>
          <span>我的二维码</span>

          <img src="/static/img/you.png" @click="ss()" alt="">
          <img style="width: 4rem;height: 4rem;" src="/static/img/erweima.png" alt="">
        </li>
        <li>
          <span>我的邀请码</span>
          <img src="/static/img/you.png" alt="" @click="yao()">
        </li>
        <li>
          <span>手机号</span>
          <span>未绑定</span>
          <router-link to="/phone"><img src="/static/img/you.png" alt=""></router-link>
        </li>
      </ul>

    </div>

    </div>
</template>

<script>
    export default {
        name: "Grxx",
        methods:{
          ss(){
            this.$router.push("/erweima");
          },
          yao(){
            this.$router.push("/yaoqingma");
          }
        }
    }
</script>

<style scoped>
  .wrap{
    margin: 0;
    padding: 0;
    width:72rem;
    height: 128rem;
    background-color:rgb(242,242,242) ;

  }
  .toubu{
    position: relative;
    width: 72rem;
    height: 9.6rem;

    background-color: rgb(229,62,66);
    text-align: left;
  }
  .toubu img{
    position: absolute;
    left:2rem;
    top: 3rem;
    width: 2.3rem;
    height: 3.8rem;
  }
  .p1{
    font-size: 3.6rem;
    color: white;
    line-height: 9.6rem;
    text-align: center;
  }
  .center{
    width: 100%;
    height: 55rem;
    background-color: #fff;
    text-align: left;
  }
  .ul1{
    list-style-type: none;
    position: relative;
  }

  .ul1 li{
    height: 10rem;
    line-height: 10rem;
    border-bottom: 1px solid #ccc;
  }
  .ul1 li:first-child{
    height: 14rem;
    line-height: 14rem;
    position: relative;
  }

  .ul1 span:nth-child(1){
    font-size: 2.8rem;
    margin-left: 2rem;

  }
  .ul1 span:nth-child(2){
    font-size: 2.8rem;
    margin-left: 48rem;
  }
  .ul1 img{
    margin-left: 2rem;
  }
  .ul1 li:nth-child(3)>img{
    float: right;
    margin-right: 1.5rem;
    margin-top: 3rem;
  }
  .ul1 li:nth-child(4)>img{
    float: right;
    margin-right: 1.5rem;
    margin-top: 3rem;
  }
  .ul1 img{
    width: 1.4rem;
    height: 2.4rem;
  }
  .span1{
    width: 10rem;
    height: 10rem;
    border-radius: 50%;
    border: 1px solid #ccc;
    font-size: 2.4rem;
    position: absolute;
    right: 5rem;
    top: 2rem;
  }
  .span1 p:first-child{
    position: absolute;
    right: 2.5rem;
    top: -3rem;
  }
  .span1 p:last-child{
    position: absolute;
    right: 2.5rem;
    top: 0.5rem;
  }
  .ul1 li:first-child img{
    position: absolute;
    right: 1.5rem;
    top: 6rem;
  }
</style>
