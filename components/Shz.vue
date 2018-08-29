<template>
    <div class="wrap">
      <div class="toubu"></div>
      <div class="zuo">
        <router-link to="/geren"><img src="/static/img/zuo.png" alt=""></router-link>
      </div>
      <p class="p1">我的神灯值</p>
       <div class="gd">
         <img src="/static/img/gengduo.png" alt="">
       </div>
       <div class="shouye">
       <div class="sun"></div>
         <div class="tm">
           <img src="/static/img/tuoyuan2.png" alt="">
         </div>
         <p class="name">昵称</p>
         <div class="num">100</div>
         <div class="s1">
           <img src="/static/img/niaohu.png" alt="">
         </div>
         <div class="tmd">
           <img src="/static/img/tuoyuan3.png" alt="">
         </div>
         <div class="wh">
           <img src="/static/img/wenhao.png" alt="">
         </div>
          <p class="gz">神灯规则</p>
         <div class="sm">
           <img src="/static/img/bantuoyuan.png" alt="">
         </div>
         <p class="year">今年购物抵钱已省</p>
         <div class="zero">
           0 ¥
         </div>
         <div class="zm">
           <img src="/static/img/banyuan.png" alt="">
         </div>
         <div class="shu">
           <img src="/static/img/shu.png" alt="">
         </div>
         <div class="ding">
           今年神灯值抵扣订单
         </div>
         <div class="zeb">
           0笔
         </div>
       </div>
      <div class="jl">
        <div class="wenben">
          <img src="/static/img/wenben.png" alt="">
        </div>
        <div class="dhj">
          兑换记录
        </div>
        <div class="right">
          <router-link to="jilu"><img src="/static/img/you.png" alt=""></router-link>
        </div>
      </div>
      <div class="jl1">
        <div class="alad">
          <img src="/static/img/niaohu1.png" alt="">
        </div>
        <div class="dhj1">
          神灯值明细
        </div>
        <div class="right1">
          <router-link to="mingxi"><img src="/static/img/you.png" alt=""></router-link>
        </div>
    </div>
      <div class="sli">
        <img src="/static/img/heng.png" alt="">
      </div>
      <div class="love">
         神灯值猜你喜欢
      </div>
      <div class="zuoh">
        <img src="/static/img/heng.png" alt="">
      </div>

      <div class="one">
        <div v-for="(item,index) in arr" class="hufu">
          <img class="hufu02" src="/static/img/04.png" alt="">
          <div class="ms">
            <span>蜗牛时装BB霜5g</span><br>
            <span class="zhi">500</span> <img src="/static/img/niaohu.png" alt="">
            <div class="xian"></div> <p class="jiage">¥22.5</p>
          </div>
        </div>



      </div>
      </div>
</template>

<script>
    export default {
        name: "Shz",
      data(){
        return{
          arr:[1,2,3,4]
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
    left: 28rem;
    top: 3rem;
  }
  .gd img{
    position: absolute;
    width: 3.4rem;
    height: 0.9rem;
    top: 5rem;
    left: 67rem;
  }
  .shouye{
    position: absolute;
  background-color: rgb(229,62,66);
    width: 72rem;
    height: 32rem;
    top: 9.7rem;
  }
  .sun{
    position: absolute;
    background-color:rgb(255,255,255);
    border-radius: 25rem;
    width: 10rem;
    height: 10rem;
    top: 2rem;
    left: 32rem;
  }
  .tm img{
    position: absolute;
    width: 4.2rem;
    height: 10rem;
    left: -0.5rem;
  }
  .tmd img{
    position: absolute;
    width: 10.9rem;
    height: 15.8rem;
    left: 62rem;
    top: 8rem;
  }
  .wh img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    left: 56rem;
    top: 2rem;
  }
  .gz{
    position: absolute;
    font-size: 2.4rem;
    color: white;
    left: 60rem;
    top: 2rem;
  }
  .name{
    position: absolute;
    font-size: 2.4rem;
    color: white;
    left: 35rem;
    top: 13rem;
  }
  .num{
    position: absolute;
    font-size:4.8rem;
    color:rgb(255,210,31);
    left: 32rem;
    top: 16rem;
  }
  .s1 img{
    position: absolute;
    width: 4rem;
    height: 2.6rem;
    top: 19rem;
    left: 41rem;
  }
  .sm img{
    position: absolute;
    width: 58.4rem;
    height: 8rem;
    left: -1rem;
    top: 24rem;
  }
  .year{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(255,255,255);
    top: 25rem;
    left: 7rem;
  }
  .zero{
    position: absolute;
   font-size: 3rem;
    color: white;
    top: 28rem;
    left: 15rem;
  }
  .zm img{
    position: absolute;
    width: 57.7rem;
    height: 8rem;
    left: 15rem;
    top: 24rem;
  }
  .shu img{
    position: absolute;
    width: 0.2rem;
    height: 6rem;
    left: 36rem;
    top: 25rem;
  }
  .ding{
    position: absolute;
    font-size: 2.4rem;
    color: white;
    left: 45rem;
    top: 25rem;
  }
  .zeb{
    position: absolute;
    font-size: 3rem;
    color: white;
    left: 53rem;
    top: 28rem;
  }
  .jl{
    position: absolute;
    width: 72rem;
    height: 8rem;
    /*border: 0.5px solid grey;*/
    background-color: white;
    top: 41.7rem;
  }
  .wenben img{
    position: absolute;
    width: 3rem;
    height: 3.1rem;
    left: 2rem;
    top:2rem;
  }
  .dhj{
   position: absolute;
   font-size: 2.8rem;
    color: #666666;
    top: 2rem;
    left: 7rem;
  }
  .right img{
    position: absolute;
    width: 1rem;
    height: 1.8rem;
    top: 3rem;
    left: 69rem;
  }
  .jl1{
    position: absolute;
    width: 72rem;
    height: 8rem;
    border: 0.5px solid grey;
    background-color: white;
    top: 50rem;
  }
  .alad img{
    position: absolute;
    width: 4rem;
    height: 2.6rem;
    left: 2rem;
    top:2rem;
  }
  .dhj1{
    position: absolute;
    font-size: 2.8rem;
    color: #666666;
    top: 2rem;
    left: 7rem;
  }
  .right1 img{
    position: absolute;
    width: 1rem;
    height: 1.8rem;
    top: 3rem;
    left: 69rem;
  }
  .sli img{
    position: absolute;
    background-color: rgb(204,204,204);
    width: 15rem;
    height: 0.2rem;
    top: 63rem;
    left: 8rem;
  }
  .love{
    position: absolute;
    font-size: 3rem;
    top: 61rem;
    left: 25rem;
    color: #666666;
    font-family: MicrosoftYaHei;
  }
  .zuoh img{
    position: absolute;
    background-color: rgb(204,204,204);
    width: 15rem;
    height: 0.2rem;
    top: 63rem;
    left: 48rem;
  }
  .one{
    position: absolute;
    top: 68rem;
    width: 100%;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    background-color: #fff;
  }
  .hufu{
    width: 33rem;
    height: 41rem;
    border: 1px #cccccc solid;
    text-align: center;

  }
  .hufu02{
    width: 6.4rem;
    height: 14.2rem;
    margin-top: 6.4rem;
  }
  .ms{
    border-top: 1px #cccccc solid;
    margin-top: 10rem;
    font-size: 2.4rem;
    position: relative;
  }
  .ms img{
    width: 2.4rem;
    height: 1.6rem;
  }
  .zhi{
    color: red;
  }
  .xian{
    position: absolute;
    width: 7rem;
    height: 0.2rem;
    background-color: #808080;
    left: 13rem;
    bottom: 1.2rem;
  }
  .jiage{
    font-size: 2.2rem;
    color: #808080;
  }
</style>

