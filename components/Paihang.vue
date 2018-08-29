<template>
   <div class="wrap">
     <div class="toubu">
     </div>
     <div class="zuo">
       <img src="/static/img/zuo.png" alt="">
     </div>
     <p class="p1">我的返金排行</p>
     <div class="skt">
       <div class="jr">
        <div class="sz">
          <span>0~499元</span>
          <span>500~999元</span>
          <span>1000~1499元</span>
         </div>
         <div class="right">
           <img src="/static/img/you.png" alt="">
         </div>
         <div class="date">
           2017/06/26
         </div>
         <div class="xf">
           消费 : ¥100
         </div>
         <div class="ph">
           排号 : 10
         </div>
       </div>
       <div class="jr1">
         <div class="date1">
           2017/06/26
         </div>
         <div class="xf1">
           消费 : ¥100
         </div>
         <div class="ph1">
           排号 : 10
         </div>
     </div>
       <div class="jr2">
         <div class="date2">
           2017/06/26
         </div>
         <div class="xf2">
           消费 : ¥100
         </div>
         <div class="ph2">
           排号 : 10
         </div>
   </div>
       <div class="jr3">
         <div class="date3">
           2017/06/26
         </div>
         <div class="xf3">
           消费 : ¥100
         </div>
         <div class="ph3">
           排号 : 10
         </div>
   </div>
   </div>
     </div>
</template>

<script>
    export default {
        name: "Paihang"
    }
</script>

<style scoped>
  .wrap{
    margin: 0;
    padding: 0;
    width: 100%;
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
    left: 30rem;
    top: 3rem;
  }
  .skt{
    position: relative;
    border: 0.5px solid gray;
    width: 72rem;
    height:41rem;
  }
  .jr{
    position: absolute;
    border: 0.5px solid gray;
    width: 72rem;
    height: 8rem;
    top: 9.8rem;

  }
  .sz{
    font-size: 3rem;
    height: 8rem;
    line-height: 8rem;
    display: flex;
    justify-content: space-around;
  }
  .sz span:hover{
    color: #f00;
  }

  .right img{
    position: absolute;
    width: 1rem;
    height: 1.8rem;
    top: 2.8rem;
    left: 70rem;
  }
  .date{
    position: absolute;
    font-size: 2.8rem;
    top: 9rem;
    left: 4rem;
  }
  .xf{
    position: absolute;
    font-size: 2.8rem;
    top: 9rem;
    left: 32rem;
  }
  .ph{
    position: absolute;
    font-size: 2.8rem;
    top: 9rem;
    left: 57rem;
  }
  .jr1{
    position: absolute;
    border: 0.5px solid gray;
    width: 72rem;
    height: 8rem;
    top: 33rem;
  }
  .date1{
    position: absolute;
    font-size: 2.8rem;
    top: 2.5rem;
    left: 4rem;
  }
  .xf1{
    position: absolute;
    font-size: 2.8rem;
    top: 2.5rem;
    left: 32rem;
  }
  .ph1{
    position: absolute;
    font-size: 2.8rem;
    top: 2.5rem;
    left: 57rem;
  }
  .jr2{
     position: absolute;
     border: 0.5px solid gray;
     width: 72rem;
     height: 8rem;
     top: 25rem;
   }
  .date2{
    position: absolute;
    font-size: 2.8rem;
    top: 2.5rem;
    left: 4rem;
  }
  .xf2{
    position: absolute;
    font-size: 2.8rem;
    top: 2.5rem;
    left: 32rem;
  }
  .ph2{
    position: absolute;
    font-size: 2.8rem;
    top: 2.5rem;
    left: 57rem;
  }
  .jr3{
    position: absolute;
    border: 0.5px solid gray;
    width: 72rem;
    height: 8rem;
    top: 41rem;
  }
  .date3{
    position: absolute;
    font-size: 2.8rem;
    top: 2.5rem;
    left: 4rem;
  }
  .xf3{
    position: absolute;
    font-size: 2.8rem;
    top: 2.5rem;
    left: 32rem;
  }
  .ph3{
    position: absolute;
    font-size: 2.8rem;
    top: 2.5rem;
    left: 57rem;
  }
</style>
