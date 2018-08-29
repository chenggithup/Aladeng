<template>
 <div class="wrap">
   <div class="toubu">

   </div>
   <div class="zuo">
     <img src="/static/img/zuo.png" alt="" @click="fan()">
   </div>
   <p class="p1">消息中心</p>
   <p class="p2">2017年06月20日10:44</p>
   <div class="two">
       <div class="tj"></div>
      <p class="p3">新品推荐</p>
     <div class="zheng">
       <img src="/static/img/zhengfangxing.png" alt="">
     </div>
     <div class="huo">
       <img src="/static/img/huo.png" alt="">
     </div>
     <div class="t1">
       <p>新品上市啦 ! 时间不多了 , 赶紧行动起</p>
     </div>
     <div class="t2">
       <p>来吧 !</p>
     </div>
     <div class="xian"></div>
     <div class="ck">
       <p>查看更多</p>
     </div>
     <div class="you">
       <img src="/static/img/you.png" alt="">
     </div>
     <p class="sj">2017年06月20日11:12</p>
   </div>
<div class="zhongjian">
    <div class="wrm">
    <p>安全提醒</p>
    </div>
  <div class="jg">
    <img src="/static/img/zhengfangxing.png" alt="">
  </div>
  <div class="waming">
    <img src="/static/img/jinggao.png" alt="">
  </div>
  <div class="zp">
    <p>近期有不法分子冒充阿拉灯客服进行诈</p>
  </div>
  <div class="pian">
    <p>骗 ,请认准阿拉灯官方客服电话</p>
  </div>
  <div class="tel">
    <p>4000123456</p>
  </div>
  <div class="shijian"><p>2017年06月20日11:12</p></div>
</div>
   <div class="slider">
     <div class="sh">
       收货啦
     </div>
     <div class="zh">
       <img src="/static/img/zhengfangxing.png" alt="">
     </div>
     <div class="liwu">
       <img src="/static/img/shouhuo.png" alt="">
     </div>
     <div class="hd">
       你的货物到站了 ,请注意查收哦~
     </div>
   </div>
 </div>

</template>

<script>
    export default {
        name: "Xiaoxi",
        methods:{
          fan(){
            this.$router.push("/shouye");
          }
        }
    }
</script>

<style scoped>
.wrap{
  margin: 0;
  padding: 0;
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
    top: 4rem;
    width: 2.3rem;
    height: 3.8rem;
  }
  .p1{
    position: absolute;
    font-size: 3.6rem;
    color: white;
    left: 30rem;
    top: 4rem;
  }
  .p2{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(128,128,128);
    font-family: "American Typewriter";
    left:23rem ;
    top: 12rem;
  }
  .tj{
    position: absolute;
    border: 1px solid rgb(204,204,204);
    font-size: 3rem;
    top: 18rem;
    left: 2rem;
    width: 68rem;
    height: 32rem;
  }
  .p3{
    position: absolute;
    font-size: 3rem;
    color: rgb(77,77,77);
    top: 19rem;
    left: 3rem;
  }
  .zheng img{
    position: absolute;
   left: 4rem;
    top: 25rem;
    width: 13rem;
    height: 14rem;
  }
  .huo img{
    position: absolute;
    left: 7rem;
    top: 28rem;
    width: 7rem;
    height: 8rem;
  }
  .t1 p{
    position: absolute;
    font-size: 2.8rem;
    top: 24rem;
    left: 19rem;
  }
  .t2 p{
    position: absolute;
    font-size: 2.8rem;
    top: 28rem;
    left: 19rem;
  }
  .xian{
    position: absolute;
    border: 1px solid grey;
    width: 64.8rem;
    height: 0.1rem;
    top: 41rem;
    left: 3rem;
  }
  .ck p{
    position: absolute;
   font-size: 2.8rem;
    top: 44rem;
    left: 3rem;
  }
  .you img{
    position:absolute;
    width: 1.4rem;
    height: 2.4rem;
    top: 44rem;
    left: 67rem;
  }
  .sj{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(128,128,128);
    font-family: "American Typewriter";
    left:23rem ;
    top: 52rem;
  }
  .zhongjian{
    margin: 0;
    padding: 0;
    border: 1px solid grey;
    width: 68rem;
    height: 24rem;
    top: 59rem;
    left: 2rem;
    position: relative;
  }
  .wrm p{
    position: absolute;
    font-size: 3rem;
    color: rgb(77,77,77);
    top: 1rem;
    left: 1rem;
  }
  .jg img{
    position: absolute;
    left: 2rem;
    top: 7rem;
    width: 13rem;
    height: 14rem;
  }
  .waming img{
    position: absolute;
    width: 7.4rem;
    height: 6.5rem;
    left: 5rem;
    top: 10rem;
  }
  .zp p{
    position: absolute;
    font-size: 2.8rem;
    top: 6.5rem;
    left: 17rem;
    color:rgb(128,128,128);
  }
  .pian{
    position: absolute;
    font-size: 2.8rem;
    color:rgb(128,128,128);
    left: 17rem;
    top: 10rem;
  }
  .tel p{
    position: absolute;
    font-size: 2.8rem;
    color:rgb(128,128,128);
    top: 14rem;
    left: 17rem;
  }
  .shijian p{
    position: absolute;
    font-size: 2.8rem;
    top:26rem;
    left: 23rem;
    font-family: "American Typewriter";
    color: rgb(128,128,128);
  }
  .slider{
    margin: 0;
    padding: 0;
    border: 1px solid grey;
    width: 68rem;
    height: 24rem;
    top: 68rem;
    left: 2rem;
    position: relative;
  }
  .sh{
   position: absolute;
    font-size: 3rem;
    left: 1rem;
    top: 1rem;
  }
  .zh img{
    position: absolute;
    left: 2rem;
    top: 7rem;
    width: 13rem;
    height: 14rem;
  }
  .liwu img{
    position: absolute;
    top: 11rem;
    left: 5rem;
    width: 6.6rem;
    height: 6.6rem;
  }
  .hd{
    position: absolute;
    font-size: 2.8rem;
    top: 6.5rem;
    left:16rem ;
    color: rgb(128,128,128);
  }
</style>
