<template>
  <div class="wrap">
    <div class="toubu">
      <img src="/static/img/youxiang.png" alt="">
      <p class="p1">个人中心</p>
      <img src="/static/img/xiaoxi.png" alt="" @click="li()">
      <img src="/static/img/shezhi.png" alt="">
    </div>
    <div class="nicheng">
      <div></div>
      <p><span  @click="hh()">登录</span>/<span @click="zhu()">注册</span></p>
      <button>账户提现</button>
    </div>
    <div class="peisong">
      <span>我的订单</span>
      <span>查看更多订单></span>
    </div>
    <div class="ding">
      <img src="/static/img/daizhifu.png" alt="">
      <img src="/static/img/daifahuo.png" alt="">
      <img src="/static/img/daishouhuo.png" alt="">
      <img src="/static/img/jiaoyiwancheng.png" alt="">
    </div>
    <div class="sp">
      <span>待支付</span>
      <span>待发货</span>
      <span>待收货</span>
      <span>交易完成</span>
    </div>
    <div>
      <div class="peisong">
        <span>我的返金排号</span>
        <span>查看更多<img src="/static/img/xiajian.png" alt="" @click="ll()"> </span>
      </div>
      <ul class="price" v-show="bol">
        <li>
          <span>2017/06/26</span>
          <span>消费 : ¥ 100</span>
          <span>排号 : 10</span>
        </li>
        <li>
          <span>2017/06/26</span>
          <span>消费 : ¥ 100</span>
          <span>排号 : 10</span>
        </li>
        <li>
          <span>2017/06/26</span>
          <span>消费 : ¥ 100</span>
          <span>排号 : 10</span>
        </li>
        <li>
          <span>2017/06/26</span>
          <span>消费 : ¥ 100</span>
          <span>排号 : 10</span>
        </li>
      </ul>

    </div>
    <div v-show="bol">
      <div class="peisong" style="margin-top: -5.5rem">

      </div>
      <ul class="price">
        <li>
          <span>2017/06/26</span>
          <span>消费 : ¥ 100</span>
          <span>排号 : 10</span>
        </li>
        <li>
          <span>2017/06/26</span>
          <span>消费 : ¥ 100</span>
          <span>排号 : 10</span>
        </li>
        <li>
          <span>2017/06/26</span>
          <span>消费 : ¥ 100</span>
          <span>排号 : 10</span>
        </li>
        <li>
          <span>2017/06/26</span>
          <span>消费 : ¥ 100</span>
          <span>排号 : 10</span>
        </li>
      </ul>

    </div>


    <div class="ding ding1" style="margin-top: 2rem">
      <img src="/static/img/shimingrenzheng.png" alt="">
      <img src="/static/img/shouhuodizhi.png" alt="">
      <img src="/static/img/guanzhugongzhonghao.png" alt="">
      <img src="/static/img/kefu.png" alt="">
    </div>
    <div class="sp">
      <span>实名认证</span>
      <span>收货地址</span>
      <span>关注公众号</span>
      <span>客服与反馈</span>
    </div>
    <div class="bottom">
      <div>
        <router-link to="/shouye"><img @click="de()" class="m1" style="width:4.8rem;height: 4.8rem;" src="/static/img/shouyeqian.png" alt=""></router-link>
        <p class="pp1">首页</p>
      </div>
      <div @click="fen()">
        <router-link to="/fenlei"><img class="i1" style="width:4.8rem;height: 4.8rem;" src="/static/img/fenleiqian.png" alt=""></router-link>
        <p>分类</p>
      </div>
      <router-link to="/dhuowang"><div>
        <img style="width:11.3rem;height: 5.5rem;" src="/static/img/duanhuo.png" alt="">
      </div></router-link>
      <router-link to="/nopur"><div>
        <img @click="mm()" class="m2" style="width: 5rem;height: 4.8rem;" src="/static/img/gouwuche.png" alt="">
        <p class="pp2">购物车</p>
      </div></router-link>
      <div>
        <router-link to="dz"><img style="width: 4.3rem;height: 4.8rem;" src="/static/img/geren.png" alt=""></router-link>
        <p>个人中心</p>
      </div>
    </div>
    <div style="height: 50rem;background-color: #f2f2f2;"></div>
    <div class="ce" v-show="bol1">
      <img src="/static/img/chahao.png" alt="" @click="mq()">
      <button @click="cc()">登录</button>
      <button @click="zz()">注册</button>
    </div>
    <div class="de" v-show="bols">
      <span @click="reg()">注册</span>
      <span>快速登录</span>
      <span>密码登录</span>
      <p>新用户首次登录自动注册阿拉灯账号</p>
      <input type="text" class="ph" value="" placeholder="请输入手机号">
      <div class="shu1"></div>
      <img src="/static/img/shouji.png" alt="">
      <input class="inp2" type="text" value="" placeholder="请输入手机验证码">
      <div class="shu2"></div>
      <img src="/static/img/yanzhengma.png" alt="">
      <button class="yanz" @click="hj()">获取验证码</button>
      <div class="ddu">
        <button @click="login">登录</button>
        <button @click="can">取消</button>
      </div>
    </div>

    <div class="de ee" v-show="bols1">
      <span>密码登录</span>
      <span>注册</span>
      <span @click="fast()">快速登录</span>
      <p>我们将发送验证码到您填写的手机号上,请注意查收</p>
      <input class="ph" type="text" value="" placeholder="请输入手机号">
      <div class="shu1"></div>
      <img src="/static/img/shouji.png" alt="">
      <input class="inp2" type="text" value="" placeholder="请输入手机验证码">
      <div class="shu2"></div>
      <img src="/static/img/yanzhengma.png" alt="">
      <button class="yanz" @click="hj()">获取验证码</button>
      <div class="ddu">
        <button @click="login">完成注册</button>
        <button @click="can">取消</button>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Zhuye",
    data(){
      return{
        bol:false,
        bol1:false,
        bols:false,
        bols1:false
      }
    },
    methods:{
      ll(){
        this.bol = !this.bol;
        this.bols = false;
        this.bols1 = false;
      },
      li(){
        this.$router.push("/xiaoxi");
      },
      hh(){
        document.getElementsByClassName("ce")[0].style.webkitZIndex=100;
        document.getElementsByClassName("peisong")[0].style.opacity="0";
        document.getElementsByClassName("peisong")[1].style.opacity="0";
        document.getElementsByClassName("nicheng")[0].style.opacity="0";
        document.getElementsByClassName("ding")[0].style.opacity="0";
        document.getElementsByClassName("ding1")[0].style.opacity="0";
        document.getElementsByClassName("sp")[0].style.opacity="0";
        document.getElementsByClassName("sp")[1].style.opacity="0";
        document.getElementsByClassName("price")[0].style.opacity="0";
        document.getElementsByClassName("price")[1].style.opacity="0";
        this.bol1 = !this.bol1;
        $(".ce button:eq(0)").css("background","#f00");
        $(".ce button:eq(0)").css("color","#fff");
      },
      zhu(){
        document.getElementsByClassName("ce")[0].style.webkitZIndex=100;
        document.getElementsByClassName("peisong")[0].style.opacity="0";
        document.getElementsByClassName("peisong")[1].style.opacity="0";
        document.getElementsByClassName("nicheng")[0].style.opacity="0";
        document.getElementsByClassName("ding")[0].style.opacity="0";
        document.getElementsByClassName("ding1")[0].style.opacity="0";
        document.getElementsByClassName("sp")[0].style.opacity="0";
        document.getElementsByClassName("sp")[1].style.opacity="0";
        document.getElementsByClassName("price")[0].style.opacity="0";
        document.getElementsByClassName("price")[1].style.opacity="0";
        this.bol1 = !this.bol1;
        $(".ce button:eq(1)").css("background","#f00");
        $(".ce button:eq(1)").css("color","#fff");
      },
      mq(){
        document.getElementsByClassName("peisong")[0].style.opacity="1";
        document.getElementsByClassName("peisong")[1].style.opacity="1";
        document.getElementsByClassName("nicheng")[0].style.opacity="1";
        document.getElementsByClassName("ding")[0].style.opacity="1";
        document.getElementsByClassName("ding1")[0].style.opacity="1";
        document.getElementsByClassName("sp")[0].style.opacity="1";
        document.getElementsByClassName("sp")[1].style.opacity="1";
        document.getElementsByClassName("price")[0].style.opacity="1";
        document.getElementsByClassName("price")[1].style.opacity="1";
        this.bol1 = !this.bol1;
        this.bols1=false;
        this.bols=false;
        $(".ce button:eq(0)").css("background","#f2f2f2");
        $(".ce button:eq(0)").css("color","#000");
        $(".ce button:eq(1)").css("background","#f2f2f2");
        $(".ce button:eq(1)").css("color","#000");
        document.getElementsByClassName("ce")[0].style.webkitZIndex=-2;
      },
      cc(){
        this.bols=!this.bols;
      },
      zz(){
        this.bols1=!this.bols1;
      },
      fast(){
        this.bols1=!this.bols1;
        this.bols=!this.bols;
      },
      reg(){
        this.bols1=!this.bols1;
        this.bols=!this.bols;
      },

      hj(){
        var a= 60;
        var myreg = /^(((13[0-9]{1})|(15[0-9]{1})|(18[0-9]{1}))+\d{8})$/;
        if(!myreg.test($(".ph").val()))
        {
          alert('请输入有效的手机号码！');
          return false;
        }else {
            $(".yanz").html(a);
            clearInterval(time);
            var time = setInterval(function(){
              a-=1;
              $(".yanz").html(a+"秒");
              if (a==0){
                $(".yanz").html('重新获取');
                clearInterval(time);
              }

            },1000);
            setTimeout(function () {
              var aa = Math.floor(Math.random()*(999999-0)+0);
              $(".inp2").val(aa);
            },10000);
        }
      },
      login(){
        this.$router.push("/geren");
      },
      can(){
        this.bols=false;
        this.bols1=false;
      }
    }
  }
</script>

<style scoped>
  .wrap{
    margin: 0;
    padding: 0;
    /*height: 200rem;*/
    background-color: #f2f2f2;
    overflow-x: hidden;
    overflow-y: scroll;
  }
  .toubu{
    position: relative;
    border: 1px solid rgb(229,62,66);
    width: 100%;
    height: 9.6rem;
    line-height: 9.6rem;
    text-align: center;
    background-color: rgb(229,62,66);
  }
  .toubu p{
    margin-top: 1rem;
    font-size: 3.6rem;
    color: white;
  }
  .toubu img{
    width: 3.6rem;
    height: 3.6rem;
  }
  .toubu img:nth-child(1){
    position: absolute;
    left: 2rem;
    top: 3rem;

  }
  .toubu img:nth-child(3){
    position: absolute;
    right: 10rem;
    top: 3rem;
  }
  .toubu img:nth-child(4){
    position: absolute;
    right: 3rem;
    top: 3rem;
  }
  .nicheng{
    width: 100%;
    height: 24rem;
    background-color: #fee3e3;
    position: relative;
  }
  .nicheng div{
    position: absolute;
    left: 2rem;
    top: 4rem;
    width: 10.5rem;
    height: 10.5rem;
    border-radius: 50%;
    background-color: #e38e8e;
  }
  .nicheng p{
    font-size: 3rem;
    position: absolute;
    left: 14rem;
    top: 16rem;
  }
  .nicheng button{
    width: 15rem;
    height: 4.2rem;
    border-radius: 2rem;
    background-color: #d26060;
    color: #fff;
    position: absolute;
    right: 4rem;
    bottom: 4rem;
    font-size: 2.4rem;
  }
  .peisong{
    height: 6rem;
    line-height: 6rem;
    margin-top: 2rem;
    background-color: #fff;
    border-bottom: 1px solid #ccc;
  }
  .peisong span:first-child{
    font-size: 2.8rem;
    float: left;
    margin-left: 2rem;
  }
  .peisong span:last-child{
    font-size: 2.8rem;
    float: right;
    margin-right: 2rem;
  }
  .peisong span img{
    width: 2.5rem;
    height: 1.4rem;
  }
  .ding{
    display: flex;
    justify-content: space-around;
    background-color: #fff;
  }
  .ding img{
    width: 3.2rem;
    height: 2.7rem;
    padding-top: 2rem;
  }
  .sp{
    padding-top: 2rem;
    padding-bottom: 2rem;
    display: flex;
    justify-content: space-around;
    background-color: #fff;
  }
  .sp span{
    font-size: 2.4rem;
  }
  .price{
    width: 100%;
    height: 24.4rem;
    background-color: #fff;
    border-bottom: 1px solid #ccc;
  }
  .price li{
    height: 6.1rem;
    line-height: 6.1rem;
    border-bottom: 1px solid #ccc;
  }
  .price li span:first-child{
    float: left;
    font-size: 2.8rem;
    margin-left: 2rem;
  }
  .price li span:nth-child(2){
    font-size: 2.8rem;
  }
  .price li span:last-child{
    float: right;
    font-size: 2.4rem;
    margin-right: 6rem;
  }
  .ding1{
    border-top: 1px solid #ccc;
    display: flex;
    justify-content: space-around;
  }
  .ding1 img{
    width: 4.3rem;
    height: 3.6rem;
  }
  .ding2{
    margin-top: 2rem;
    padding-top: 6rem;
  }
  .ding2 p{
    font-size: 3rem;
    color: #f00;
    margin-top: -4rem;
  }
  .bottom{
    margin-top: 30rem;
    position: fixed;
    left: 0;
    bottom: 0;
    background-color: #fff;
    display: flex;
    justify-content: space-around;
    width: 100%;
    height: 9.7rem;
    text-align: center;
    line-height: 9.7rem;
    border-top: 1px solid #e6e6e6;
  }
  .bottom img{
    margin-top: 1.5rem;
  }
  p{
    margin-top: -8rem;
    font-size: 2rem;
    color: #666666;
  }
  .ce{
    position: absolute;
    left: 0;
    bottom: 0;
    height: 36rem;
    width: 100%;
    background-color: #fff;
  }
  .ce img{
    float: right;
    width: 2.4rem;
    height: 2.4rem;
  }
  .ce button{
    width: 60rem;
    height: 6rem;
    background-color: #f2f2f2;
    border-radius: 2rem;
    font-size: 2.8rem;
  }
  .ce button:nth-child(2){
    margin-top: 6rem;
  }
  .ce button:nth-child(3){
    margin-top: 6rem;
    margin-left: -2rem;
  }
  .ce button:hover{
    background-color: #f00;
    color: #fff;
  }
  .de{
    width: 90%;
    height: 40rem;
    text-align: left;
    background-color: #fff;
    margin-left: 3rem;
    overflow: hidden;
    position: relative;
    padding-bottom: 2rem;
    position: absolute;
    left: 1rem;
    top: 44rem;
  }
  .de span{
    font-size: 2.4rem;
    padding-left: 14rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid #ccc;

  }
  .de span:nth-child(1){
    margin-left: -8rem;
  }
  .de span:nth-child(2){
    font-size: 3rem;
  }
  .de p{
    border-top: 1px solid #ccc;
    margin-top: 2rem;
    padding-top: 2rem;
    font-size: 1.8rem;
    margin-left: 20rem;
  }
  .de input:nth-child(5){
    width: 60.8rem;
    height: 6rem;
    line-height: 6rem;
    border: 1px solid #ccc;
    border-radius: 2rem;
    margin-top: 2rem;
    margin-left: 2rem;
    font-size: 2.4rem;
    text-align: center;
  }
  input::-webkit-input-placeholder {
    /* placeholder字体大小  */
    font-size: 2.4rem;
    /* placeholder位置  */
    text-align: center;
  }
  .de input:nth-child(8){
    width: 38.8rem;
    height: 6rem;
    line-height: 6rem;
    border: 1px solid #ccc;
    border-radius: 2rem;
    margin-top: 2rem;
    margin-left: 2rem;
    font-size: 2.4rem;
    text-align: center;
  }
  .de button{
    width: 20.6rem;
    height: 6rem;
    line-height: 6rem;
    border-radius: 2rem;
    background-color: #f2f2f2;
    font-size: 2.4rem;
    position: absolute;
    right: 2rem;
    bottom: 15rem;
  }
  .de img:nth-last-of-type(1){
    position: absolute;
    left: 4rem;
    top: 15rem;
  }
  .de img:nth-last-of-type(2){
    position: absolute;
    left: 4rem;
    top: 23rem;
  }
  .shu1,.shu2{
    width: 0.1rem;
    height: 3rem;
    background-color: #ccc;
  }
  .shu1{
    position: absolute;
    left: 7rem;
    top: 14.5rem;
  }
  .shu2{
    position: absolute;
    left: 7rem;
    top: 22.5rem;
  }
  .ddu{
    width: 100%;
    margin-top: 2rem;
  }
  .ddu button:first-child{
    position: absolute;
    left: 50%;
    top: 30rem;
    width: 50%;
    height: 8rem;
    font-size: 2.4rem;
  }
  .ddu button:last-child{
    position: absolute;
    left: 0;
    top: 30rem;
    width: 50%;
    height: 8rem;
    font-size: 2.4rem;
  }
  .ddu button:hover{
    color: #ff0000;
  }
</style>

