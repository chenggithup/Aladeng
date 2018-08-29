<template>
  <div class="wrap">
    <div class="toubu"></div>
    <div class="zuo">
      <img src="/static/img/zuo.png" alt="">
    </div>
    <p class="p1">添加新地址</p>
    <p class="p2">完成</p>
    <p class="nn1">请使用您的真实姓名，否则订单将无法发出</p>
    <div class="nam1">
      <input  class="inp1" type="text" placeholder="李四">
    </div>
    <div class="phone1">
      <input type="text" placeholder="15012340708">
    </div>
    <div class="city1">
      <p>河南省新乡市红旗区</p>
      <img src="/static/img/you.png" alt="">
    </div>
    <div class="ad1">
      <input type="text" placeholder="请填写详细地址">
    </div>
    <div class="yb1">
      <input type="text" placeholder="请填写邮编">
    </div>
  </div>
</template>
<script>
  export default {
    name: "Add2"
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
  .p2{
    position: absolute;
    font-size: 3rem;
    color: white;
    left: 62rem;
    top: 3.5rem;
  }
  .nn1{
    position: absolute;
    font-size: 2.4rem;
    color:rgb(229,62,66);
    top: 12rem;
    left: 2rem;
  }
  .nam1 input{
    position: absolute;
    width: 72rem;
    font-size: 2.8rem;
    height: 10rem;
    background-color: rgb(255,255,255);
    top: 17rem;
    border: 1px solid rgb(204,204,204);
    left: -0.1rem;
  }
  .phone1 input{
    position: absolute;
    width: 72rem;
    font-size: 2.8rem;
    height: 10rem;
    background-color: rgb(255,255,255);
    top: 29rem;
    border: 1px solid rgb(204,204,204);
    left: -0.1rem;
  }
  .city1{
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color: rgb(255,255,255);
    top: 39.2rem;
  }
  .city1 p{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(128,128,128);
    top: 2.5rem;
  }
  .city1 img{
    position: absolute;
    width: 1rem;
    height:1.8rem;
    top: 3.5rem;
    left: 70rem;
  }
  .ad1 input{
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color:rgb(255,255,255);
    top: 49.4rem;
    border: 1px solid rgb(204,204,204);
    left: -0.1rem;
    font-size: 2.8rem;
  }
  .yb1 input {
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color:rgb(255,255,255);
    border: 1px solid rgb(204,204,204);
    top: 59.6rem;
    font-size: 2.8rem;
    left: -0.1rem;
  }
</style>
