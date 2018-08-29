<template>
<div class="wrap">
  <div class="toubu"></div>
  <div class="zuo">
    <router-link to="/shiming1"><img src="/static/img/zuo.png" alt=""></router-link>
  </div>
  <p class="p1">身份实名认证</p>
  <router-link to="/shiming1"><p class="p2">添加新身份</p></router-link>
  <div class="geren1">
   <p class="p3">李四</p>
    <p class="p4">410781************</p>
    <div class="zhengmian">
      <p>身份证正面照片</p>
    </div>
    <div class="fanmian">
      <p>身份证反面照片</p>
    </div>
  </div>
  <div class="bc">
   <div class="ssc">
     <img src="/static/img/shanchu.png" alt="" @click="shan()">
   </div>
     <p class="p5" @click="shan()">删除</p>
    <div class="bbj">
      <img src="/static/img/bianji.png" alt="">
    </div>
    <p class="p6">编辑</p>
  </div>
  <div class="geren11">
    <p class="pp3">李四</p>
    <p class="pp4">410781************</p>
    <div class="zhengmian1">
      <p>身份证正面照片</p>
    </div>
    <div class="fanmian1">
      <p>身份证反面照片</p>
    </div>
       <p class="ppp">审核通过</p>
  </div>
  <div class="bc1">
    <div class="ssc1">
      <img src="/static/img/shanchu.png" alt="" @click="chu()">
    </div>
    <p class="pp5" @click="chu()">删除</p>
    <div class="bbj1">
      <img src="/static/img/bianji.png" alt="">
    </div>
    <p class="pp6">编辑</p>
  </div>
</div>
</template>

<script>
    export default {
        name: "Shiming2",
        methods:{
          shan(){
            $(".geren1").remove();
            $(".bc").remove();
          },
          chu(){
            $(".geren11").remove();
            $(".bc1").remove();
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
    left: 25rem;
    top: 3rem;
  }
  .p2{
    position: absolute;
    font-size: 3rem;
    color: white;
    left: 55rem;
    top: 3.5rem;
  }
  .geren1{
    position: absolute;
    width: 72rem;
    height: 24rem;
    border: 1px solid gray;
     background-color:rgb(255,255,255);
    top: 9.8rem;
  }
  .p3{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    left: 2rem;
    top: 0.5rem;
  }
  .p4{
    position: absolute;
    font-size: 2.8rem;
    left: 18rem;
    top: 1rem;
  }
  .zhengmian{
    position: absolute;
    width: 20rem;
    height: 12rem;
    border: 1px solid rgb(204,204,204);
    top: 8rem;
    left: 2rem;
  }
  .zhengmian p{
    position: absolute;
    font-size:1.8rem;
    top:5rem;
    left: 3rem;
  }
  .fanmian{
    position: absolute;
    width: 20rem;
    height: 12rem;
    border: 1px solid rgb(204,204,204);
    top: 8rem;
    left: 25rem;
  }
  .fanmian p {
    position: absolute;
    font-size: 1.8rem;
    top: 5rem;
    left: 3rem;
  }
  .bc{
    position: absolute;
    width: 72rem;
    height: 8rem;
    background-color: rgb(255,255,255);
    top: 34rem;
  }
  .ssc img{
    position:absolute;
    width: 3rem;
    height: 3rem;
    top: 2rem;
    left: 60rem;
  }
  .p5{
    position: absolute;
    font-size: 2.4rem;
    left: 65rem;
    top: 2rem;
  }
  .bbj img{
    position:absolute;
    width: 3rem;
    height: 3rem;
    top: 2rem;
    left: 47rem;
  }
  .p6 {
    position: absolute;
    font-size: 2.4rem;
    left: 52rem;
    top: 2rem;
  }
  .geren11{
    position: absolute;
    width: 72rem;
    height: 24rem;
    background-color:rgb(255,255,255);
    top: 42.5rem;
  }
  .pp3{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    left: 2rem;
    top: 0.5rem;
  }
  .pp4{
    position: absolute;
    font-size: 2.8rem;
    left: 18rem;
    top: 1rem;
  }
  .zhengmian1{
    position: absolute;
    width: 20rem;
    height: 12rem;
    border: 1px solid rgb(204,204,204);
    top: 8rem;
    left: 2rem;
  }
  .zhengmian1 p{
    position: absolute;
    font-size:1.8rem;
    top:5rem;
    left: 3rem;
  }
  .fanmian1{
    position: absolute;
    width: 20rem;
    height: 12rem;
    border: 1px solid rgb(204,204,204);
    top: 8rem;
    left: 25rem;
  }
  .fanmian1 p {
    position: absolute;
    font-size: 1.8rem;
    top: 5rem;
    left: 3rem;
  }
  .bc1{
    position: absolute;
    width: 72rem;
    height: 8rem;
    background-color: rgb(255,255,255);
    top: 66.7rem;
  }
  .ssc1 img{
    position:absolute;
    width: 3rem;
    height: 3rem;
    top: 2rem;
    left: 60rem;
  }
  .pp5{
    position: absolute;
    font-size: 2.4rem;
    left: 65rem;
    top: 2rem;
  }
  .bbj1 img{
    position:absolute;
    width: 3rem;
    height: 3rem;
    top: 2rem;
    left: 47rem;
  }
  .pp6 {
    position: absolute;
    font-size: 2.4rem;
    left: 52rem;
    top: 2rem;
  }
  .ppp{
    position: absolute;
    font-size: 3rem;
    color:rgb(87,182,35);
    left:58rem;
    top: 1rem;
  }
</style>
