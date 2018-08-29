<template>
  <div v-if="bol" class="wrap">
    <div class="nav">
      <span class="span1">阿拉灯</span>
      <input class="inp" type="text" value="" placeholder="输入商品关键字" @click="dian()">
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
    <div class="re">
      <div class="head">
        <div></div>
        <p>热销类目</p>
        <div></div>
      </div>
      <div class="center">
        <div>
          <img src="/static/img/20.png" alt="">
          <p>糖果</p>
        </div>
        <div>
          <img src="/static/img/penghua.png" alt="">
          <p>膨化</p>
        </div>
        <div>
          <img src="/static/img/paomian.png" alt="">
          <p>方便面</p>
        </div><div>
        <img src="/static/img/qiaokeli.png" alt="">
        <p>巧克力</p>
      </div>
      </div>
    </div>
    <div class="jp">
      <div class="head">
        <div></div>
        <p>爆品推荐</p>
        <div></div>
      </div>
      <div class="cen">
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
      <div class="cen">
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
      <div class="cen cen1">
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
  import Lunbo from '@/components/Lunbo'
  import axios from 'axios'
  export default {
    name: "Meishi",
    data(){
      return{
        bol:false,
        arr:[]
      }
    },
    components:{
      Lunbo
    },
    methods:{
      dian(){
        this.$router.push("/xiaoxi");
      }
    },
    mounted:function () {
      axios.get('/api/phph0302/zh01.php').then((res)=>{
        this.bol = true;
        this.arr=res.data;
      })

    }
  }
</script>

<style scoped>
  .wrap{
    width: 100%;
    background-color: #f2f2f2;
    overflow-y: scroll;
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
  .re{
    background-color: #fff;
    position: relative;
    margin-top: 9rem;
    height: 36rem;
  }
  .head div:first-child{
    position: absolute;
    left: 21rem;
    top: 5rem;
  }
  .head div:last-child{
    position: absolute;
    left: 43.3rem;
    top: 5rem;
  }
  .head{
    background-color: #fff;
    z-index: 2;
    height: 6rem;
    line-height: 6rem;
  }
  .head div{
    width: 10%;
    height: 0.1rem;
    background-color: #cccccc;
    text-align: center;
  }
  .head p{
    padding-top: 2rem;
    font-size: 3rem;
  }
  .center{
    margin-top: 4rem;
    display: flex;
    justify-content: space-around;
  }
  .center img{
    width: 11.6rem;
    height: 11rem;
  }
  .center p{
    margin-top: 5rem;
    font-size: 2.4rem;
  }
  .jp{
    margin-top: 12rem;
    position: relative;
  }
  .cen{
    width: 100%;
    background-color: #fff;
    overflow: hidden;
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

  .bottom{
    margin-top: 10rem;
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
  .cen1{
    margin-bottom: 10rem;
  }

</style>
