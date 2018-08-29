<template>
  <div class="wrap">
    <div class="toubu">
      <img src="/static/img/youxiang.png" alt="">
      <p class="p1">个人中心</p>
      <img src="/static/img/xiaoxi.png" alt="" @click="li()">
      <img src="/static/img/shezhi.png" alt="" @click="she()">
    </div>
    <div class="nicheng">
      <router-link to="grxx"><div></div></router-link>
      <p>昵称</p>
      <router-link to="zhanghu"><button>账户提现</button></router-link>
    </div>
    <div class="peisong">
      <span>我的订单</span>
      <router-link to="/quanbu"><span>查看更多订单></span></router-link>
    </div>
    <div class="ding">
      <img src="/static/img/daizhifu.png" alt="" @click="fr()">
      <img src="/static/img/daifahuo.png" alt="" @click="fr()">
      <img src="/static/img/daishouhuo.png" alt="" @click="fr()">
      <img src="/static/img/jiaoyiwancheng.png" alt="" @click="fr()">
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
    <div class="ding ding1 ding2">
      <router-link to="shz"><p>0</p></router-link>
      <p>0</p>
      <p>0</p>
      <router-link to="/xindede"><p>0</p></router-link>
    </div>
    <div class="sp">
      <span>我的神灯值</span>
      <span>我的积分</span>
      <span>我的优惠券</span>
      <span>我的心得</span>
    </div>

    <div class="ding ding1">
      <router-link to="/shiming"><img src="/static/img/shimingrenzheng.png" alt=""></router-link>
      <router-link to="/address"><img src="/static/img/shouhuodizhi.png" alt=""></router-link>
      <router-link to="/gzh"><img src="/static/img/guanzhugongzhonghao.png" alt=""></router-link>
      <router-link to="/fankui"><img src="/static/img/kefu.png" alt=""></router-link>
    </div>
    <div class="sp">
      <span>实名认证</span>
      <span>收货地址</span>
      <span>关注公众号</span>
      <span>客服与反馈</span>
    </div>
    <div class="bottom">
      <div>
        <router-link to="/shouye"><img class="m1" style="width:4.8rem;height: 4.8rem;" src="/static/img/shouyeqian.png" alt=""></router-link>
        <p class="pp1">首页</p>
      </div>
      <div @click="fen()">
        <router-link to="/fenlei"><img class="i1" style="width:4.8rem;height: 4.8rem;" src="/static/img/fenleiqian.png" alt=""></router-link>
        <p>分类</p>
      </div>
      <router-link to="/dhuowang"><div>
        <img style="width:11.3rem;height: 5.5rem;" src="/static/img/duanhuo.png" alt="">
      </div></router-link>
      <router-link to="/gouwu"><div>
        <img class="m2" style="width: 5rem;height: 4.8rem;" src="/static/img/gouwuche.png" alt="">
        <p class="pp2">购物车</p>
      </div></router-link>
      <div>
        <router-link to="dz"><img style="width: 4.3rem;height: 4.8rem;" src="/static/img/geren.png" alt=""></router-link>
        <p>个人中心</p>
      </div>
    </div>
    <div style="height: 10rem"></div>
  </div>
</template>

<script>
  export default {
    name: "Geren",
    data(){
      return{
        bol:false
      }
    },
    methods:{
      fr(){
        this.$router.push('/quanbu');
      },
      ll(){
        this.bol = !this.bol;
      },
      li(){
        this.$router.push("/xiaoxi");
      },
      she(){
        this.$router.push('/qingchu');
      }
    }
  }
</script>

<style scoped>
  .wrap{
    margin: 0;
    padding: 0;
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
</style>

