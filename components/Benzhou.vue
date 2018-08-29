<template>
    <div v-if="bol" class="wrap">
      <div class="pp0"></div>
      <div class="tou">
        <img src="/static/img/zuo.png" alt="" @click="bd()">
        <p>本周新品</p>
        <img src="/static/img/fenfen.png" alt="" @click="fenx()">
      </div>
      <div class="tm">
        <p>本周新品</p>
        <span>精选环球好物</span>
      </div>
      <div class="cm">
        <div>
          <input class="inp" type="text" value="" placeholder="输入商品关键字">
          <img class="sousuo" src="/static/img/sousuo.png" alt="">
        </div>
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
      <div class="tu"><img src="/static/img/dingbu.png" alt="" @click="dingbu()"></div>
      <div v-show="bols" class="fenx">
        <ul>
          <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height: 6.4rem;"  src="/static/img/pengyouquan.png" alt=""><span>朋友圈</span> </a> </li>
          <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height:6.4rem;"  src="/static/img/weixin.png" alt=""><span>微信好友</span> </a> </li>
          <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height:6.4rem;"  src="/static/img/QQ.png" alt=""><span>QQ好友</span> </a> </li>
          <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height:6.4rem;"  src="/static/img/QQkongjian.png" alt=""><span>QQ空间</span> </a> </li>
          <li><a href="https://www.sina.com.cn/">   <img style="width: 6.4rem;height: 6.4rem;" src="/static/img/weibo.png" alt=""> <span>新浪微博</span> </a> </li>
          <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height: 6.4rem;"  src="/static/img/fuzhilianjie.png" alt=""><span>复制链接</span> </a> </li>

        </ul>
        <button @click="ml()">取消</button>
      </div>
    </div>
</template>

<script>
    import axios from 'axios'
    export default {
        name: "Benzhou",
      data(){
        return{
          bols:false,
          bol:false,
          arr:[]
        }
      },
        methods:{
          bd(){
            this.$router.push('/muying')
          },
          dingbu(){
            $('html,body').animate({scrollTop:0},'slow');
          },
          fenx(){
            this.bols=true;
            document.getElementsByClassName("kl")[0].style.opacity="0.1";
            document.getElementsByClassName("pp0")[0].style.webkitZIndex="100";
            document.getElementsByClassName("tm")[0].style.opacity="0.1";
          },
          ml(){
            this.bols=!this.bols;
            document.getElementsByClassName("kl")[0].style.opacity="1";
            document.getElementsByClassName("pp0")[0].style.webkitZIndex="-1";
            document.getElementsByClassName("tm")[0].style.opacity="1";
          }
        },
      mounted:function () {
        axios.get('/api/phph0302/zh01.php').then((res)=>{
          this.bol=true;
          this.arr=res.data;
        })
      }
    }
</script>

<style scoped>
  .pp0{
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 63rem;
    background-color: rgba(0,0,0,0.01);
    z-index: -1;
  }
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
    width: 3.6rem;
    height: 3.6rem;
    position: absolute;
    right: 2rem;
    top: 2rem;
  }
  .tm{
    width: 100%;
    background-color: #fff;
    position: relative;
    /*border: 1px solid black;*/
    height: 14rem;
  }
  .tm p{
    font-size: 3.6rem;
    color: #e53e42;
    position: absolute;
    left: 2rem;
    top: 2rem;
  }
  .tm span{
    font-size: 3rem;
    position: absolute;
    left: 2rem;
    top: 8rem;
  }
  .cm{
    margin-top: 2rem;
    height: 8.7rem;
    width: 100%;
  }
  .cm div{
    width: 94%;
    height: 5rem;
    border-radius: 1rem;
    text-align: center;
    margin-left: 2rem;
    background-color: #fff;
    position: relative;
  }
  .inp{
    width: 40rem;
    height: 5rem;
    border-radius: 1rem;
    font-size: 2.4rem;
    text-align: center;
  }
  .inp::-webkit-input-placeholder {
    /* placeholder颜色  */
    color: #e53e42;
    /* placeholder字体大小  */
    font-size: 2.4rem;
    /* placeholder位置  */
    text-align: center;
  }
  .sousuo{
    width: 2.8rem;
    height: 3rem;
    position: absolute;
    left: 22rem;
    top: 1rem;
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
  .tu{
    position: fixed;
    right: 0;
    bottom: 0;
  }
  .tu img{
    width: 4.8rem;
    height: 4.8rem;
  }
  .fenx{
    width: 100%;
    height: 45rem;
    background-color: white;
    position: fixed;
    left: 0;
    bottom: 0;
    z-index: 2;
  }
  .fenx ul{
    margin-top: 2rem;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  .fenx ul li{
    font-size: 2rem;
    margin-bottom: 15px;
    display: block;
    height: 15rem;
    width: 33%;
    position: relative;
  }
  .fenx ul li span{
    font-size: 2.4rem;
    position: absolute;
    left: 8rem;
    top: 8rem;
  }
  .fenx ul li a {
    color: #555;
    display: block;
    text-decoration:none;
  }
  .fenx button{
    font-size: 2.4rem;
    width:17rem;
    height: 5.5rem;
    color:white;
    border-radius: 2rem;
    background:red;
  }
</style>
