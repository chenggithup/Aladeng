<template>
    <div class="wrap">
      <div class="toubu"></div>
      <div class="zuo">
        <router-link to="/grxx"><img src="/static/img/zuo.png" alt=""></router-link>
      </div>
      <p class="p1">我的二维码</p>
      <div class="dd">
        <img src="/static/img/gengduo.png" alt="" @click="dl()">
      </div>
      <div class="center">
        <div class="ri"></div>
        <div class="name">
          昵称
        </div>
        <div class="ma">
          <img src="/static/img/erweima.png" alt="">
        </div>
        <div class="saoma">
          扫一扫上面二维码图案，邀请好友注册吧
        </div>
      </div>
      <div class="bottom" v-show="bol">
        <ul class="ul1">
          <li>分享二维码</li>
          <li @click="save()">保持到手机</li>
          <li @click="cancel()">取消</li>
        </ul>
      </div>
    </div>
</template>

<script>
    export default {
        name: "Erweima",
        data(){
          return{
            bol:false
          }
        },
        methods:{
          dl(){
            this.bol=true;
            $(".center").css("opacity","0.1");
          },
          save(){
            alert("保存到手机成功!");
            this.bol=false;
            $(".center").css("opacity","1");
          },
          cancel(){
            this.bol=false;
            $(".center").css("opacity","1");
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
    left: 30rem;
    top: 3rem;
  }
  .dd img{
    position: absolute;
    width: 3.4rem;
    height: 0.9rem;
    top: 5rem;
    left: 65rem;
  }
  .ri{
    position: absolute;
    border:1px solid rgb(227,142,142);
    width: 10rem;
    height: 10rem;
    border-radius: 5rem;
    background-color: rgb(227,142,142);
    top: 15rem;
    left: 2rem;
  }
  .name{
    position: absolute;
   font-size: 3rem;
    color: #666666;
    top: 18rem;
    left: 15rem;
  }
  .ma img{
    position: absolute;
    width: 27.6rem;
    height: 27.8rem;
    top: 35rem;
    left: 20rem;
  }
  .saoma{
  position: absolute;
    font-size: 2.8rem;
    top: 67rem;
    left: 10rem;
    color: #666666;
  }
  .bottom{
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 30rem;
    background-color: #fff;
  }
  .ul1{
    list-style-type: none;
    font-size: 2.4rem;
  }
  .ul1 li{
    height: 10rem;
    border-bottom: 1px solid #ccc;
    line-height: 10rem;
  }
</style>
