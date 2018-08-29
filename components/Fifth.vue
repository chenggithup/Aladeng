<template>
   <div class="ac">
     <div class="ou">
       <Third></Third>
       <First style="margin-top: 2rem"></First>
       <Second style="margin-top: 2rem"></Second>
       <Forth style="margin-top: 2rem"></Forth>
       <div class="peisong" style="margin-top: 2rem">
         <span>订单编号:485269676465</span>
         <span>已取消</span>
       </div>
       <ul class="ul1">
         <li class="li2">
           <div class="shangp">
             <img class="om" src="/static/img/wuyanse.png" alt="" @click="jh()">
             <img src="/static/img/01.png" alt="">
             <img src="/static/img/01.png" alt="">
             <img src="/static/img/01.png" alt="">
             <img src="/static/img/01.png" alt="">
           </div>
         </li>
       </ul>
       <div class="bottom">
         <p>实付:<span>¥166.06</span></p>
       </div>
       <div class="peisong" style="margin-top: 2rem">
         <span>订单编号:485269676465</span>
         <span>交易关闭</span>
       </div>
       <ul class="ul1">
         <li class="li2">
           <div class="shangp">
             <img class="om" src="/static/img/wuyanse.png" alt="" @click="jh()">
             <img src="/static/img/01.png" alt="">
             <img src="/static/img/01.png" alt="">
             <img src="/static/img/01.png" alt="">
             <img src="/static/img/01.png" alt="">
           </div>
         </li>
       </ul>
       <div class="bottom">
         <p>实付:<span>¥166.06</span></p>
       </div>
     </div>
   </div>
</template>

<script>
  import First from '@/components/First'
  import Second from '@/components/Second'
  import Third from '@/components/Third'
  import Forth from '@/components/Forth'
    export default {
        name: "Fifth",
        components:{
          First,
          Second,
          Third,
          Forth
        }
    }
</script>

<style scoped>
  .ac{
    height: 100%;
    position: relative;

  }
  .ac p{
    position: absolute;
    right: 3rem;
    top: -16.5rem;
    font-size: 3.6rem;
    color: #ffffff;
  }
  .peisong{
    height: 6rem;
    line-height: 6rem;
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
    color: #f00;
  }
  .ul1{
    list-style-type: none;
    background-color: #fff;
  }
  .li2{
    position: relative;
    width: 100%;
    height: 20rem;
    border-bottom:1px #cccccc solid;
  }
  .shangp{
    position: absolute;
    left: 10rem;
    top:5rem;
    width: 32.9rem;
    height: 14.1rem;
  }
  .shangp img{
    width: 8.6rem;
    height: 10rem;
    position: absolute;
    left: 1rem;
  }
  .shangp img:nth-child(1){
    width: 3rem;
    height: 3rem;
    position: absolute;
    left: -6rem;
    top: 4rem;
    display: none;
  }
  .shangp img:nth-child(2){
    position: absolute;
    left: 18rem;
    top: 0rem;
  }
  .shangp img:nth-child(3){
    position: absolute;
    left: 35rem;
    top: 0rem;
  }
  .shangp img:nth-child(4){
    position: absolute;
    left: 52rem;
    top: 0rem;
  }
  .shangp p{
    position: absolute;
    left: 15rem;
    top: 10rem;
    font-size: 2.8rem;
    color: #808080;
    width: 18.9rem;
  }
  .bottom{
    width: 100%;
    height: 8.8rem;
    position: relative;
    background-color: #fff;
  }
  .bottom p{
    font-size: 2.8rem;
    position: absolute;
    left: -45rem;
    top: 2rem;
    color: #f00;
  }
  .bottom p span{
    font-size: 2.8rem;
    margin-left: 2rem;
    color: #f00;
  }
  .bottom button{
    width: 12.7rem;
    height: 4rem;
    background-color: #f00;
    color: #fff;
    border-radius: 2rem;
    font-size: 2.4rem;
    position: absolute;
    right: 4rem;
    top: 2rem;
  }
  .bb{
    height: 10rem;

    background-color: #fff;
    line-height: 10rem;
    position: relative;
    position: fixed;
    left: 0;
    bottom: 0;
  }
</style>
