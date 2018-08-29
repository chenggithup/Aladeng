<template>
  <div class="wrap">
    <div class="tou">
      <img src="/static/img/zuo.png" alt="" @click="bd()">
      <p>这些都是 "断货王" ...</p>
      <img src="/static/img/fenfen.png" alt="">
    </div>
    <div class="bai"></div>
    <Tui></Tui>
    <div class="xa">
      <div class="xia">
        <p>还剩1000件</p>
        <button @click="qiang()">马上去抢</button>
      </div>
      <div class="xia">
        <p>还剩1000件</p>
        <button @click="qiang()">马上去抢</button>
      </div>
      <div class="xia">
        <p>还剩1000件</p>
        <button @click="qiang()">马上去抢</button>
      </div>
    </div>
    <div class="bai1"></div>
    <Tui></Tui>
    <div class="xa">
      <div class="xia">
        <p>还剩1000件</p>
        <button @click="qiang()">马上去抢</button>
      </div>
      <div class="xia">
        <p>还剩1000件</p>
        <button @click="qiang()">马上去抢</button>
      </div>
      <div class="xia">
        <p>还剩1000件</p>
        <button @click="qiang()">马上去抢</button>
      </div>
    </div>
    <div class="bai1"></div>
    <Tui></Tui>
    <div class="xa  xia1">
      <div class="xia">
        <p>还剩1000件</p>
        <button @click="qiang()">马上去抢</button>
      </div>
      <div class="xia">
        <p>还剩1000件</p>
        <button @click="qiang()">马上去抢</button>
      </div>
      <div class="xia">
        <p>还剩1000件</p>
        <button @click="qiang()">马上去抢</button>
      </div>
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
      <router-link to="/gouwu"><div>
        <img class="m2" style="width: 5rem;height: 4.8rem;" src="/static/img/gouwuche.png" alt="">
        <p class="pp2">购物车</p>
      </div></router-link>
      <div>
        <router-link to="/dz"><img style="width: 4.3rem;height: 4.8rem;" src="/static/img/geren.png" alt=""></router-link>
        <p>个人中心</p>
      </div>
    </div>
  </div>
</template>

<script>
    import Tui from '@/components/Tui'
    export default {
        name: "Dhuowang",
        methods:{
          qiang(){
            this.$router.push("/jies");
          },
          bd(){
            this.$router.push("/shouye");
          },
          fen(){
            this.$router.push("/fenlei");
          },
          de(){
            this.n++;
            if(this.n % 2 ==0){
              document.getElementsByClassName("m1")[0].src="/static/img/shouyeqian.png";
              document.getElementsByClassName("pp1")[0].style.color= '';
            }else{
              document.getElementsByClassName("m1")[0].src="/static/img/shouyehou.png";
              document.getElementsByClassName("pp1")[0].style.color= '#f00';
            }
          }
        },
        components:{
          Tui
        }
    }
</script>

<style scoped>
  .wrap{
    width: 100%;
    background-color: #f2f2f2;
    overflow-y: scroll;
  }
  .tou{
    width: 100%;
    height: 9.6rem;
    line-height: 9.6rem;
    text-align: center;
    position: relative;
    background-color: #f00;
    margin-top: 8rem;
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
    top: 3rem;
  }
  .tou img:nth-child(3){
    width: 3.6rem;
    height: 3.6rem;
    position: absolute;
    right: 2rem;
    top: 3rem;
  }
  .bai{
    width: 100%;
    height: 6rem;
    background-color: #fff;
    border-bottom: 1px solid #ccccccc;
  }
  .xa{
    display: flex;
    justify-content: space-around;
    background-color: #fff;
    margin-top: -4rem;
    padding-bottom: 2rem;
  }
  .xia{
    border-top: 1px solid #cccccc;
    background-color: #fff;
    margin-top: 1rem;
  }
  .xia p{
    margin-top: 1rem;
    font-size: 1.8rem;
    color: #4d4d4d;
  }
  .xia button{
    width: 14rem;
    height: 3rem;
    border-radius: 2rem;
    background-color: #f00;
    color: #ffffff;
    font-size: 2rem;
    margin-top: 1rem;

  }
  .bai1{
    height: 2rem;
  }
  .xia1{
    margin-bottom: 8rem;
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
