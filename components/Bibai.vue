<template>
    <div v-if="bol1" class="wrap">
      <div class="tou">
        <img src="/static/img/zuo.png" alt="" @click="bd()">
        <p>必买清单</p>
        <img src="/static/img/more.png" alt="" @click="ca()">

      </div>
      <div class="kl">
        <div class="zj">
          <img src="/static/img/copy.png" alt="">
          <div class="zz">
            <p>奶粉也要玩有机,养成健康北鼻</p>
          </div>
        </div>
        <div class="kh">
          <img :src="arr[18].src" alt="">
        </div>

        <div class="kh1">
          <img :src="arr[18].src" alt="">
        </div>

        <div class="kh2">
          <img :src="arr[18].src" alt="">
        </div>
        <div class="by">
          <p>{{arr[18].names}}</p>
        </div>
        <div class="price">¥59</div>
        <div class="hr">
          <p>{{arr[18].names}}</p>
        </div>
        <div class="price1">{{arr[18].jiage}}</div>
        <div class="jw">
          <p>{{arr[18].names}}</p>
        </div>
        <div class="price2">¥88</div>
      </div>
      <div class="kl k2">
        <div class="zj">
          <img src="/static/img/copy.png" alt="">
          <div class="zz">
            <p>奶粉也要玩有机,养成健康北鼻</p>
          </div>
        </div>
        <div class="kh">
          <img :src="arr[18].src" alt="">
        </div>

        <div class="kh1">
          <img :src="arr[18].src" alt="">
        </div>

        <div class="kh2">
          <img :src="arr[18].src" alt="">
        </div>
        <div class="by">
          <p>{{arr[18].names}}</p>
        </div>
        <div class="price">¥59</div>
        <div class="hr">
          <p>{{arr[18].names}}</p>
        </div>
        <div class="price1">{{arr[18].jiage}}</div>
        <div class="jw">
          <p>{{arr[18].names}}</p>
        </div>
        <div class="price2">¥88</div>
      </div>
      <div class="yin"  v-show="bol">
        <ul>
          <router-link to="/xiaoxi"><li><img src="/static/img/xixi.png" alt=""> 消息</li></router-link>
          <router-link to="/shouye"><li><img src="/static/img/sgouye.png" alt=""> 首页</li></router-link>
          <li><img src="/static/img/xiang.png" alt=""> 分享</li>
          <router-link to="dz"><li><img src="/static/img/ge.png" alt=""> 个人中心</li></router-link>
        </ul>
      </div>
      <div class="bott"><img src="/static/img/dingbu.png" alt="" @click="dianji()"></div>
    </div>
</template>

<script>
  import axios from 'axios'
    export default {
        name: "Bibai",
        data(){
          return{
            bol:false,
            bol1:false,
            arr:[]
          }
        },
        methods:{
          bd(){
            this.$router.push("/kaishou");
          },
          ca(){
            this.bol=!this.bol;
          },
          dianji(){
            $('html,body').animate({scrollTop:0},'slow');
          }
        },
        mounted:function () {
          axios.get('/api/phph0302/zh01.php').then((res)=>{
            this.bol1=true;
            this.arr=res.data;
          })
        }
    }
</script>

<style scoped>
  .wrap{
    width: 100%;
    background-color: #f2f2f2;
  }
  .tou{
    width: 100%;
    height: 8rem;
    line-height: 8rem;
    text-align: center;
    position: relative;
    background-color: #f00;
  }
  .yin{
    position: absolute;
    right: 0;
    top: 8rem;
    height: 28rem;
    width: 16rem;
    border-radius: 1rem;
    border: 1px solid black;
    background-color: #fff;
  }
  .yin ul{
    list-style-type: none;
    text-align: left;
    margin-left: 2rem;
  }
  .yin ul li img{
    width: 18%;
  }
  .yin ul li{
    vertical-align: top;
    font-size: 2.4rem;
    margin-top: 3rem;
  }
  .tou p{
    font-size: 3.6rem;
    color: #ffffff;
  }
  .tou img:nth-child(1){
    width: 2.3rem;
    height: 3.8rem;
    position: absolute;
    left: 2rem;
    top: 2rem;
  }
  .tou img:nth-child(3){
    width: 3.4rem;
    height: 0.9rem;
    position: absolute;
    right: 2rem;
    top: 3.5rem;
  }
  .kl{
    position: relative;
    background-color: #fff;
    height: 76rem;
  }
  .zj{
    position: relative;
  }
  .zj .zz{
    width: 100%;
    position: absolute;
    top: 24.7rem;
    left: 0;
    text-align: center;
    background-color: #5c7d86;
    height: 8rem;
    line-height: 8rem;
    opacity: 0.5;
  }
  .zz p{
    font-size: 3rem;
    color: #fff;
    font-weight: bolder;
  }

  .zj img{
    width: 100%;
  }
  .kh{
    margin-top: 2rem;
    height: 18.8rem;
  }
  .kh img{
    position: absolute;
    width: 14.3rem;
    height: 14.3rem;
    top: 43rem;
    left: 3rem;
    border: 1px solid #cccccc;
    padding: 3rem;
  }
  .kh1{
    background-color: #fff;
  }
  .kh1 img{
    position: absolute;
    width: 14.3rem;
    height: 14.3rem;
    top: 43rem;
    left: 26rem;
    border: 1px solid #cccccc;
    padding: 3rem;
  }

  .kh2 img{
    position: absolute;
    width: 14.3rem;
    height: 14.3rem;
    top: 43rem;
    left:49rem;
    border: 1px solid #cccccc;
    padding: 3rem;
  }
  .price{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(232,61,65);
    left: 11rem;
    top: 72rem;
  }
  .by{
    position: absolute;
    font-size: 2.4rem;
    color: black;
    top: 63rem;
    left: 7rem;

  }
  .hr{
    position: absolute;
    font-size: 2.4rem;
    color: black;
    top: 63rem;
    left: 32rem;
  }
  .price1{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(232,61,65);
    left: 36rem;
    top: 72rem;
  }
  .jw{
    position: absolute;
    font-size: 2.4rem;
    color: black;
    top: 63rem;
    left: 53rem;
  }
  .price2{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(232,61,65);
    left: 57rem;
    top: 72rem;
  }
  .by p:nth-child(1){
    font-size: 2.4rem;
    margin-top: 2rem;
    margin-left: -2rem;
    width: 16rem;
  }
  .hr p:nth-child(1){
    font-size: 2.4rem;
    margin-top: 2rem;
    margin-left: -2rem;
    width: 16rem;
  }
  .jw p:nth-child(1){
    font-size: 2.4rem;
    margin-top: 2rem;
    margin-left: -2rem;
    width: 16rem;
  }
  .k2{
    margin-top: 2rem;
    background-color: #fff;
  }
  .bott{
    position: fixed;
    right: 0;
    bottom: 0;
  }
  .bott img{
    width: 4.8rem;
    height: 4.8rem;
  }
</style>
