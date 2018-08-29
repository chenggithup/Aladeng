<template>
<div v-if="bol" class="wrap">
  <div class="nav">
    <span class="span1">阿拉灯</span>
    <input class="inp" type="text" value="" placeholder="输入商品关键字">
    <img class="sousuo" src="/static/img/sousuo.png" alt="">
    <img style="width: 3.8rem;height: 3.8rem;position: absolute;right: 2.2rem;top: 3rem;" src="/static/img/xiaoxi.png" alt="" @click="dian()">
  </div>
  <div class="nave">
    <router-link to="/shouye"><span>推荐</span></router-link>
    <router-link to="/kaishou"><span>贼惦记</span></router-link>
    <router-link to="/meishi"><span>美食</span></router-link>
    <router-link to="/muying"><span>母婴</span></router-link>
  </div>
  <lunbo></lunbo>
  <div class="kl">
    <div class="maifen">
      <div class="dh"></div>
      <p class="p1">奶粉专区</p>
      <div class="dh1"></div>
    </div>
    <div class="zj">
      <img src="/static/img/mamibaobei.png" alt="" @click="bc()">
    </div>
    <div class="kh">
      <img :src="arr[18].src" alt="">
    </div>
    <div class="shu"></div>
    <div class="kh1">
      <img :src="arr[18].src" alt="">
    </div>
    <div class="shu1"></div>
    <div class="kh2">
      <img :src="arr[18].src" alt="">
    </div>
    <div class="by">
      <p>{{arr[0].names}}</p>
    </div>
    <div class="price">¥59</div>
    <div class="hr">
      <p>{{arr[1].names}}</p>
    </div>
    <div class="price1">{{arr[18].jiage}}</div>
    <div class="jw">
      <p>{{arr[2].names}}</p>
    </div>
    <div class="price2">¥88</div>
  </div>
  <div class="kl">
    <div class="maifen">
      <div class="dh"></div>
      <p class="p1">纸尿裤专区</p>
      <div class="dh1"></div>
    </div>
    <div class="zj">
      <router-link to="/bibai"><img src="/static/img/bibei.png" alt=""></router-link>
    </div>
    <div class="kh">
      <img :src="arr[19].src" alt="">
    </div>
    <div class="shu"></div>
    <div class="kh1">
      <img :src="arr[19].src" alt="">
    </div>
    <div class="shu1"></div>
    <div class="kh2">
      <img :src="arr[19].src" alt="">
    </div>
    <div class="by">
      <p>{{arr[0].names}}</p>
    </div>
    <div class="price">¥59</div>
    <div class="hr">
      <p>{{arr[1].names}}</p>
    </div>
    <div class="price1">{{arr[18].jiage}}</div>
    <div class="jw">
      <p>{{arr[2].names}}</p>
    </div>
    <div class="price2">{{arr[19].jiage}}</div>
  </div>
  <div class="cen">
    <div class="maifen">
      <div class="dh"></div>
      <p class="p1">猜你喜欢</p>
      <div class="dh1"></div>
    </div>
    <div class="left">
      <img :src="arr[15].src" alt="">
      <img src="/static/img/baopin.png" alt="">
      <p>{{arr[15].names}}</p>
      <p>{{arr[15].jiage}}</p>
    </div>
    <div class="right">
      <img :src="arr[16].src" alt="">
      <img src="/static/img/baopin.png" alt="">
      <p>{{arr[16].names}}</p>
      <p>{{arr[16].jiage}}</p>
    </div>
  </div>
  <div class="bottom">
    <div>
      <router-link to="/shouye"><img style="width:4.8rem;height: 4.8rem;" src="/static/img/shouyeqian.png" alt=""></router-link>
      <p>首页</p>
    </div>
    <div>
      <router-link to="/fenlei"><img style="width:4.8rem;height: 4.8rem;" src="/static/img/fenleiqian.png" alt=""></router-link>
      <p>分类</p>
    </div>
    <router-link to="/dhuowang"><div>
      <img style="width:11.3rem;height: 5.5rem;" src="/static/img/duanhuo.png" alt="">
    </div></router-link>
    <router-link to="/gouwu"><div>
      <img style="width: 5rem;height: 4.8rem;" src="/static/img/gouwuche.png" alt="">
      <p>购物车</p>
    </div></router-link>
    <div>
      <router-link to="dz"><img style="width: 4.3rem;height: 4.8rem;" src="/static/img/geren.png" alt=""></router-link>
      <p>个人中心</p>
    </div>
  </div>
</div>


</template>

<script>
    import axios from 'axios'
    import Lunbo from '@/components/Lunbo'
    export default {
        name: "Muying",
        data(){
          return{
            bol:false,
            arr:[]
          }
        },
      components: {
        Lunbo
      },
      methods:{
        dian(){
          this.$router.push("/xiaoxi");
        },
        bc(){
          this.$router.push("/benzhou");
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
  .wrap{
    width: 100%;
    background-color: #f2f2f2;
    position: relative;
    overflow-x: hidden;
  }
  .nav{
    background-color: #e53e42;
    width: 100%;
    height: 9.6rem;
    line-height: 9.6rem;
    position: relative;
    /*border: 1px solid black;*/
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
  .span1{
    font-size: 3.6rem;
    color: #fff;
    position: absolute;
    left: 2.4rem;
  }
  .nave{
    width: 100%;
    height: 6rem;
    display: flex;
    justify-content: space-around;
    /*border: 1px solid black;*/
    line-height: 6rem;
    padding-top: 1rem;
    background-color: #fff;
  }
  .nave span{
    font-size: 3rem;
  }
  .nave span:hover{
    color: #e83d41;
    border-bottom: 0.2rem solid #ff0000;
  }
  .kl{
    position: relative;
    background-color: #fff;
    margin-top: 2rem;
    height: 65rem;
  }
  .kh,.zj,.by{
    background-color: #fff;
  }
  .maifen{
    height: 6rem;
    background-color: #fff;
  }
.dh{
  position: absolute;
  width: 6rem;
  height: 0.1rem;
  left: 22rem;
  top: 11rem;
  background-color:#cccccc;
  }
  .p1{
    font-size: 3rem;
    position: absolute;
    top: 100rem;
    left: 30rem;
    color:#4d4d4d;
  }
  .dh1{
    position: absolute;
    width: 6rem;
    height: 0.1rem;
    top: 3rem;
    left: 44rem;
    background-color:#cccccc;
  }
  .zj{
    background-color: #fff;
  }
  .zj img{
    width: 66rem;
    padding-left: 3rem;
    padding-right: 3rem;
    height: 30rem;
  }
  .kh img{
    position: absolute;
    width: 14.3rem;
    height: 14.3rem;
    top: 39.8rem;
    left: 7rem;
  }
  .shu{
    position: absolute;
    width: 0.1rem;
    height: 17rem;
    left: 25rem;
    top: 39.8rem;
    background-color:gray;
  }
  .kh1{
    background-color: #fff;
  }
  .kh1 img{
    position: absolute;
    width: 14.3rem;
    height: 14.3rem;
    top: 39.8rem;
    left: 30rem;
  }
  .shu1{
    position: absolute;
    width: 0.1rem;
    height: 17rem;
    left: 48rem;
    top: 39.8rem;
    background-color:gray;
  }
  .kh2 img{
    position: absolute;
    width: 14.3rem;
    height: 14.3rem;
    top: 39.8rem;
    left:52rem;
  }
  .price{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(232,61,65);
    left: 12rem;
    top: 59rem;
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
    left: 34rem;
    top: 59rem;
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
    left: 55rem;
    top: 59rem;
  }
  .cen{
    margin-top: 2rem;
    width: 100%;
    background-color: #fff;
    overflow: hidden;
    position: relative;
    margin-bottom: 10rem;
  }
  .left,.right{
    width: 31rem;
    height: 28rem;
    border: 1px solid black;
    position: relative;
  }
  .left{
    float: left;
    margin-left: 3rem;
    margin-top: 4rem;
  }
  .right {
    float: left;
    margin-left: 3rem;
    margin-top: 4rem;
  }

  .left img:nth-child(1){
    width: 50%;
    margin-top: 3.8rem;
  }
  .right img:nth-child(1){
    width: 50%;
    margin-top: 10rem;
  }
  .left img:nth-child(2),.right img:nth-child(2){
    width: 4.1rem;
    height: 7.8rem;
    position: absolute;
    left: 0;
    top: 0;
  }
  .left p:nth-child(4){
    font-size: 2.4rem;
    margin-top: 0.2rem;
    color: #e53e42;
  }
  .left p:nth-child(3){
    font-size: 2.4rem;
    margin-top: 0.3rem;
  }
  .right p:nth-child(4){
    font-size: 2.4rem;
    margin-top: 0.3rem;
    color: #e53e42;
  }
  .right p:nth-child(3){
    font-size: 2.4rem;
    margin-top: 1rem;
  }
  .maifen{
    height: 6rem;
    background-color: #fff;
  }
  .dh{
    position: absolute;
    width: 6rem;
    height: 0.1rem;
    left: 22rem;
    top: 3rem;
    background-color:#cccccc;
  }
  .p1{
    font-size: 3rem;
    position: absolute;
    top: 1rem;
    left: 30rem;
    color:#4d4d4d;
    margin-top: 0rem;
  }
  .dh1{
    position: absolute;
    width: 6rem;
    height: 0.1rem;
    top: 3rem;
    left: 44rem;
    background-color:#cccccc;
  }
  .bottom{
    position: fixed;
    left: 0;
    bottom: 0;
    display: flex;
    justify-content: space-around;
    width: 100%;
    height: 9.7rem;
    text-align: center;
    line-height: 9.7rem;
    background-color: #fff;
  }
  .bottom img{
    margin-top: 1.5rem;
  }
  p{
    margin-top: -8rem;
    font-size: 2rem;
  }
  .sousuo{
    width: 2.8rem;
    height: 3rem;
    position: absolute;
    left: 24.4rem;
    top: 3.3rem;
  }
</style>
