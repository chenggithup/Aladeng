<template>
    <div class="wrap">
      <div class="toubu">
      </div>
      <div class="zuo">
        <router-link to="/geren"><img src="/static/img/zuo.png" alt=""></router-link>
      </div>
      <p class="p1">我的心得</p>
      <div class="ff">
        <img src="/static/img/fenfen.png" alt="">
      </div>
        <div class="gr">
          <div class="per">
            <img src="/static/img/ty.png" alt="">
          </div>
          <div class="pon">
            <img src="/static/img/xinderen.png" alt="">
          </div>
          <div class="name">
            昵称
          </div>
          <div class="nr">
            该模块主要内容是顾客对购买的商品的评价...该模块主要内容是
          </div>
          <div class="pj">
            顾客对购买的商品的评价...
          </div>

        </div>
      <div class="use">
        <div class="kh">
          <img src="/static/img/chuncai.png" alt="">
        </div>

      </div>
      <div class="date">
        8小时前
      </div>
      <div class="wg">
      <div class="qt">
        <div class="cc">
          <img src="/static/img/chuncai.png" alt="">
        </div>
      </div>
        <div class="hc">
          焕彩萃璨花蕊唇彩4.8g
        </div>
        <div class="usa">
          <img src="/static/img/yingguo%202.png" alt="">
        </div>
        <div class="fly">
          <img src="/static/img/feiji.png" alt="">
        </div>
        <div class="hw">
          海外直邮
        </div>
        <div class="pr">
          ¥ 166.06
        </div>
      </div>
       <div class="dibu">
         <div class="pl">
           用户评论 ( 1 )
         </div>
         <div class="heng">

         </div>
         <div class="per1">
           <img src="/static/img/ty.png" alt="">
         </div>
         <div class="pon1">
           <img src="/static/img/xinderen.png" alt="">
         </div>
         <div class="name1">
           昵称
         </div>
         <div class="nr1">
           该模块主要内容是顾客对购买的商品的评价...该模块主要内容是
         </div>
         <div class="pj1">
           其他顾客对购买的商品的评价...
         </div>
         <div class="zan">
           <img src="/static/img/dianzan.png" alt="">
         </div>
         <div class="shu">

         </div>
         <div class="dz">
           点赞
         </div>
         <div class="pingl">
           <img src="/static/img/pinglun.png" alt="">
         </div>
         <div class="xpl">
           写评论
         </div>
         <div class="shu1">

         </div>
         <div class="fen">
           <img src="/static/img/xiaofen.png" alt="">
         </div>
         <div class="fxx">
           分享
         </div>
       </div>
    </div>
</template>

<script>
    export default {
        name: "Xinde"
    }
</script>

<style scoped>
  .wrap{
    margin: 0;
    padding: 0;
    width: 100%;
    position: relative;
    background-color: #fff;
    width: 72rem;
    height: 188.8rem;
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
  .ff img{
    position: absolute;
    width: 3.6rem;
    height: 3.4rem;
    top: 4rem;
    left: 67rem;
  }
  .gr{
    position: relative;
    width: 68rem;
    height: 15.9rem;
    top: 10rem;
    left: 2rem;
  }
  .per img{
    position: absolute;
    width: 8rem;
    height: 8rem;
    top: 1.5rem;
    left:0.2rem ;
  }
  .pon img{
    position: absolute;
    width: 8rem;
    height: 8rem;
    left: 1rem;
    top: 1.5rem;
  }
  .name{
    position: absolute;
    font-size: 2.8rem;
    top: 4rem;
    left: 10rem;
    color: rgb(77,77,77);
  }
  .nr{
    position: absolute;
    font-size: 2.4rem;
    top: 10rem;
  }
  .pj{
    position: absolute;
    font-size: 2.4rem;
    top: 13rem;
  }
  .use{
    position: relative;
    border: 1px solid grey;
    width: 26rem;
    height: 20rem;
    top: 12rem;
    left: 2rem;
  }
  .kh img{
    position: absolute;
    width: 6.2rem;
    height: 13.8rem;
    top: 3rem;
    left: 10rem;
  }
  .date{
    position: absolute;
    font-size:2.4rem;
    top: 50rem;
    left: 2rem;
  }
  .wg{
    position: relative;
    border: 0.5px solid gray;
    width: 68rem;
    height: 16rem;
    top: 20rem;
    left: 2rem;
    /*background-color: white;*/
  }
  .qt{
    position: absolute;
    border: 0.5px solid gray;
    width: 18rem;
    height: 16rem;
  }
  .cc img{
    position: absolute;
    width: 6.9rem;
    height: 15.3rem;
    top: 0.5rem;
    left: 7rem;
  }
  .hc{
    position: absolute;
    font-size: 2.8rem;
    left:21rem ;
    color: rgb(77,77,77);
  }
  .usa{
    position: absolute;
    width: 3rem;
    height: 2rem;
    border: 1px solid gray;
    left: 21rem;
    top: 8rem;
  }
  .usa img{
    position: absolute;
    width: 3rem;
    height: 1.5rem;
    left: 0.1rem;
    top: 0.2rem;
  }
  .fly img{
    position: absolute;
    width:3.4rem;
    height: 3.3rem;
    top: 7rem;
    left: 25.5rem;
  }
  .hw{
    position: absolute;
    font-size: 2.4rem;
    top: 7rem;
    left: 30rem;
  }
  .pr{
    position: absolute;
    font-size: 3rem;
    color:rgb(229,62,66);
    top: 11rem;
    left: 22rem;
  }
  .dibu{
    position: relative;
    /*border: 1px solid gray;*/
    width: 72rem;
    height: 38.6rem;
    top: 22rem;
    left: 0.1rem;
    background-color: white;
  }
  .pl{
    position: absolute;
    font-size: 2.8rem;
    left: 2rem;
    top: 1.5rem;
  }
  .heng{
    position: absolute;
    border: 0.5px solid gray;
    width: 73rem;
    top: 8rem;
    left: -0.5rem;
  }
  .per1 img{
    position: absolute;
    width: 8rem;
    height: 8rem;
    top: 9.7rem;
    left:2rem ;
  }
  .pon1 img{
    position: absolute;
    width: 8rem;
    height: 8rem;
    left: 2rem;
    top: 10rem;
  }
  .name1{
    position: absolute;
    font-size: 2.8rem;
    top: 12rem;
    left: 12rem;
    color: rgb(77,77,77);
  }
  .nr1{
    position: absolute;
    font-size: 2.4rem;
    top: 19rem;
    left: 2rem;
  }
  .pj1{
    position: absolute;
    font-size: 2.4rem;
    top: 23rem;
    left: 2rem;
  }
  .zan img{
    position: absolute;
    width: 2.4rem;
    height: 2.4rem;
    top: 32rem;
    left: 10rem;
  }
  .dz{
    position: absolute;
    font-size:2.4rem;
    top: 35rem;
    left: 9rem;
  }
  .pingl img{
    position: absolute;
    width: 2.4rem;
    height: 2.3rem;
    top: 32rem;
  }
  .xpl{
    position: absolute;
    font-size: 2.4rem;
    top: 35rem;
    left: 34rem;
  }
  .shu{
    position: absolute;
    width: 0.1rem;
    height: 4rem;
    border: 1px solid gray;
    top: 33rem;
    left: 23rem;
  }
  .shu1{
    position: absolute;
    width: 0.1rem;
    height: 4rem;
    border: 1px solid gray;
    top: 33rem;
    left: 53rem;
  }
  .fen img{
    position: absolute;
    width: 2.4rem;
    height: 2.3rem;
    top: 32rem;
    left: 63rem;
  }
  .fxx{
    position: absolute;
    font-size: 2.4rem;
    top: 35rem;
    left: 62rem;
  }
</style>
