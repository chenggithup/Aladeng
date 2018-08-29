<template>
<div v-if="bol" class="wrap">
  <div class="top">
    <img @click="ba()" src="/static/img/zuo.png" alt="" class="inp">
    <div>
      <input type="text" value="" placeholder="唇彩">
      <img src="/static/img/sousuo.png" alt="" class="sousuo">
    </div>
    <div class="cg">
      <img src="/static/img/chagang.png" alt="">
    </div>
    <div class="ss">
      搜索
    </div>
  </div>
  <div class="bt">
  <div class="mr">
    默认
  </div>
    <div class="price">
      价格<img src="/static/img/jiage.png" alt="">
    </div>
    <div class="xl">
      销量
    </div>
    <div class="sx">
      筛选
    </div>
  </div>
  <div class="daigou">
    <div class="cc">
      <img :src="arr[20].src" alt="">
    </div>
    <div class="zb">
      {{arr[20].names}}
    </div>
    <div class="zz">
      {{arr[20].miaoshu}}
    </div>
    <div class="zx">
      焕彩萃璨花蕊唇彩4.8g
    </div>
    <div class="jp">
      <img src="/static/img/riben.png" alt="">
    </div>
    <div class="fly">
      <img src="/static/img/feiji.png" alt="">
    </div>
    <div class="hw">
      海外直邮
    </div>
    <div class="jia">
      {{arr[20].jiage}}
    </div>
  </div>
  <div class="daigou">
    <div class="cc">
      <img :src="arr[20].src" alt="">
    </div>
    <div class="zb">
      {{arr[20].names}}
    </div>
    <div class="zz">
      {{arr[20].miaoshu}}
    </div>
    <div class="zx">
      焕彩萃璨花蕊唇彩4.8g
    </div>
    <div class="jp">
      <img src="/static/img/riben.png" alt="">
    </div>
    <div class="fly">
      <img src="/static/img/feiji.png" alt="">
    </div>
    <div class="hw">
      海外直邮
    </div>
    <div class="jia">
      {{arr[20].jiage}}
    </div>
  </div>
  <div class="daigou">
    <div class="cc">
      <img :src="arr[20].src" alt="">
    </div>
    <div class="zb">
      {{arr[20].names}}
    </div>
    <div class="zz">
      {{arr[20].miaoshu}}
    </div>
    <div class="zx">
      焕彩萃璨花蕊唇彩4.8g
    </div>
    <div class="jp">
      <img src="/static/img/riben.png" alt="">
    </div>
    <div class="fly">
      <img src="/static/img/feiji.png" alt="">
    </div>
    <div class="hw">
      海外直邮
    </div>
    <div class="jia">
      {{arr[20].jiage}}
    </div>
  </div>
  <div class="daigou">

    <div class="cc">
      <img :src="arr[20].src" alt="">
    </div>
    <div class="zb">
      {{arr[20].names}}
    </div>
    <div class="zz">
      {{arr[20].miaoshu}}
    </div>
    <div class="zx">
      焕彩萃璨花蕊唇彩4.8g
    </div>
    <div class="jp">
      <img src="/static/img/riben.png" alt="">
    </div>
    <div class="fly">
      <img src="/static/img/feiji.png" alt="">
    </div>
    <div class="hw">
      海外直邮
    </div>
    <div class="jia">
      {{arr[20].jiage}}
    </div>
  </div>


  <div class="slider">
    <img src="/static/img/lunbo.png" alt="">
  </div>
  <div class="db">
    加载更多
  </div>
  </div>
</template>
<script>
    import axios from 'axios'
    export default {
        name: "Chuncai",
        data(){
          return{
            bol:false,
            arr:[]
          }
        },
        methods:{
          ba(){
            this.$router.push("/sousuo");
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
  *{
    margin: 0;
    padding: 0;
  }
  .wrap{
    width: 100%;
    background-color: #f2f2f2;
    position: relative;
    overflow-x: hidden;
  }
  .top{
    display: flex;
    justify-content:space-between;
    background-color: red;
    height: 11.3rem;
    line-height: 11.3rem;
    width: 100%;
  }
  .top img:nth-child(1){
    width: 2.3rem;
    height: 3.5rem;
    margin-top:3.7rem;
    margin-left: 2rem;
  }
  input{
    font-size: 2.8rem;
  }
  input::-webkit-input-placeholder {
    /* placeholder字体大小  */
    font-size: 2.8rem;
    /* placeholder位置  */
    text-align: center;
  }
  .top div{
    text-align: center;
    width: 54.3rem;
    height: 6rem;
  }
  .top div input{
    position: absolute;
    top: 2.5rem;
    left: 8rem;
    width: 54.3rem;
    height: 6rem;
    border-radius: 1rem;
  }
  .sousuo{
    width: 2.8rem;
    height: 3rem;
    position: absolute;
    left: 10rem;
    top: 4rem;
  }
  .cg img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    left: 56rem;
  }
  .ss{
    position: absolute;
   font-size: 3rem;
    left: 40rem;
    color: rgb(255,255,255);
  }
  .bt{
    position:relative;
    width: 72rem;
    height: 8rem;
    top: 0.1rem;
    background-color: #fff;
  }
  .mr{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(229,62,66);
    left: 3rem;
    top: 2rem;
  }
  .price{
    position: absolute;
    font-size: 2.8rem;
    top: 2rem;
    left: 21rem;
  }
  .price img{
    width: 0.8rem;
    height: 1.7rem;
    margin-left: 1rem;
  }
  .xl{
    position: absolute;
    font-size: 2.8rem;
    top: 2rem;
    left: 42rem;
  }
  .sx{
    position: absolute;
    font-size: 2.8rem;
    top: 2rem;
    left: 62rem;
  }
  .daigou{
    position: relative;
    width: 100%;
    height: 20rem;
    border:1px solid gray;
    background-color: #fff;
    margin-top: 2rem;
  }

  .cc img{
    position: absolute;
    width: 6.9rem;
    height:15.3rem;
    top: 2rem;
    left: 7.5rem;
  }
  .zb{
    position: absolute;
    font-size: 3rem;
    color: rgb(51,51,51);
    font-family: SimHei;
    left: 20rem;
    top:1rem;
  }
  .zz{
    position: absolute;
  font-size: 2.4rem;
  color:rgb(77,77,77);
  left: 20rem;
  top: 6rem;
  }
  .zx{
    position: absolute;
    font-size: 2.4rem;
    color:rgb(77,77,77);
    left: 20rem;
    top: 10rem;
  }
  .jp img{
    position: absolute;
    width: 3rem;
    height: 2rem;
    top: 15.3rem;
    left: 21rem;
  }
  .fly img{
    position: absolute;
    width: 3.4rem;
    height: 3.3rem;
    top: 14.5rem;
    left: 26rem;
  }
  .hw{
    position: absolute;
    font-size: 2.4rem;
    top: 14.5rem;
    left: 30rem;
  }
  .jia{
    position: absolute;
    font-size: 3rem;
    color: rgb(229,62,66);
    top: 15rem;
    left: 58rem;
  }

  .jp3 img{
    position: absolute;
    width: 3rem;
    height: 2rem;
    top: 15.3rem;
    left: 21rem;
  }
  .fly3 img{
    position: absolute;
    width: 3.4rem;
    height: 3.3rem;
    top: 14.5rem;
    left: 26rem;
  }
  .slider{
    margin-top: 2rem;
  }
  .slider img{
    width: 72rem;
    height: 30rem;
  }
  .db{
    font-size: 2.4rem;
    margin-top: 2rem;
    height: 7.3rem;
    line-height: 7.3rem;
    color: grey;
  }
</style>
