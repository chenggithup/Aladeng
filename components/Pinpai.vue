<template>
  <div v-if="bol" class="wrap">
    <div class="toubu"></div>
    <div class="zjt">
      <img src="/static/img/zuo.png" alt="" @click="ff()">
    </div>
    <p class="pp">品牌精选</p>
    <div class="fx1">
      <img src="/static/img/fengxiang.png" alt="">
    </div>
    <div class="diyilan">
      <img src="/static/img/haba.png" alt="">
    </div>
    <div class="t1">
      <img :src="arr[4].src" alt="">
    </div>
    <div class="t2">
      <img :src="arr[4].src" alt="">
    </div>
    <div class="t3">
      <img :src="arr[5].src" alt="">
    </div>
    <div class="wl">
      {{arr[4].names}}
    </div>
    <div class="pirce">
      {{arr[4].jiage}}
    </div>
    <div class="wl1">
      {{arr[4].names}}
    </div>
    <div class="pirce1">
      {{arr[4].jiage}}
    </div>
    <div class="G1">
      {{arr[5].names}}
    </div>
    <div class="pirce2">
      {{arr[5].jiage}}
    </div>
    <div class="dierlan">
      <img src="/static/img/haba.png" alt="">
    </div>
    <div class="t4">
      <img :src="arr[4].src" alt="">
    </div>
    <div class="t5">
      <img :src="arr[4].src" alt="">
    </div>
    <div class="t6">
      <img :src="arr[5].src" alt="">
    </div>
    <div class="wl2">
      {{arr[4].names}}
    </div>
    <div class="pirce3">
      {{arr[4].jiage}}
    </div>
    <div class="wl3">
      {{arr[4].names}}
    </div>
    <div class="pirce4">
      {{arr[4].jiage}}
    </div>
    <div class="G2">
      {{arr[5].names}}
    </div>
    <div class="pirce5">
      {{arr[5].jiage}}
    </div>
    <div class="dibu">
      <img src="/static/img/dingbu.png" alt="">
    </div>
    <div class="jiantou">
      <img src="/static/img/xiangshang.png" alt="">
    </div>
  </div>
</template>
<script>
  import axios from "axios"
    export default {
        name: "Pinpai",
        data(){
          return{
            bol:false,
            arr:[]
          }
        },
        methods:{
          ff(){
            this.$router.push("/shouye");
          }
        },
      mounted:function () {
        axios.get('/api/phph0302/zh01.php').then((res)=>{
          this.bol = true;
          this.arr=res.data;
          console.log(this.arr);
        })
      }
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
  .zjt img{
    position: absolute;
    left:3rem;
    top: 4rem;
    width: 2.3rem;
    height: 3.8rem;
  }
  .pp{
    position: absolute;
    font-size: 3.6rem;
    color: white;
    left: 27rem;
    top: 3.5rem;
  }
  .fx1 img{
    position: absolute;
    width: 3.6rem;
    height: 3.4rem;
    top: 4.5rem;
    left: 63rem;
  }
  .diyilan img{
    position: absolute;
    width: 72rem;
    height: 30rem;
    top: 10rem;
    left: 0.1rem;
  }
  .t1 img{
    position: absolute;
    top: 41rem;
    left: 1rem;
    border: 1px solid grey;
    width: 22.4rem;
    height: 22.6rem;
  }
  .t2 img{
    position: absolute;
    top: 41rem;
    left: 24.5rem;
    border: 1px solid grey;
    width: 22.4rem;
    height: 22.6rem;
  }
  .t3 img{
    position: absolute;
    top: 41rem;
    left: 48rem;
    border: 1px solid grey;
    width: 22.4rem;
    height: 22.8rem;
  }
  .wl{
    position: absolute;
    top: 65rem;
    left:1rem ;
    font-size: 1.8rem;
    color:rgb(77,77,77) ;
  }
 .pirce{
   position: absolute;
   font-size: 2rem;
   color: rgb(229,62,66);
   top: 68rem;
   left: 3rem;
 }
  .wl1{
    position: absolute;
    top: 65rem;
    left:25rem ;
    font-size: 1.8rem;
    color:rgb(77,77,77) ;
  }
  .pirce1{
    position: absolute;
    font-size: 2rem;
    color: rgb(229,62,66);
    top: 68rem;
    left: 27rem;
  }
  .G1{
    position: absolute;
    top: 65.2rem;
    left:50rem ;
    font-size: 1.8rem;
    color:rgb(77,77,77) ;
  }
  .pirce2{
    position: absolute;
    font-size: 2rem;
    color: rgb(229,62,66);
    top: 68rem;
    left: 53rem;
  }
  .dierlan img{
    position: absolute;
    width: 72rem;
    height: 30rem;
    top: 73rem;
    left: 0.1rem;
  }
  .t4 img{
    position: absolute;
    top: 104rem;
    left: 1rem;
    border: 1px solid grey;
    width: 22.4rem;
    height: 22.6rem;
  }
  .t5 img{
    position: absolute;
    top: 104rem;
    left: 24.5rem;
    border: 1px solid grey;
    width: 22.4rem;
    height: 22.6rem;
  }
  .t6 img{
    position: absolute;
    top: 104rem;
    left: 48rem;
    border: 1px solid grey;
    width: 22.4rem;
    height: 22.8rem;
  }
  .wl2{
    position: absolute;
    top: 128rem;
    left:2rem ;
    /*background-color: red;*/
    font-size: 1.8rem;
    color:rgb(77,77,77) ;
  }
  .pirce3{
    position: absolute;
    font-size: 2rem;
    color: rgb(229,62,66);
    top: 131rem;
    left: 3rem;
  }
  .wl3{
    position: absolute;
    top: 128rem;
    left:25rem ;
    font-size: 1.8rem;
    color:rgb(77,77,77) ;
  }
  .pirce4{
    position: absolute;
    font-size: 2rem;
    color: rgb(229,62,66);
    top: 131rem;
    left: 27rem;
  }
  .G2{
    position: absolute;
    top: 128rem;
    left:50rem ;
    font-size: 1.8rem;
    color:rgb(77,77,77) ;
  }
  .pirce5{
    position: absolute;
    font-size: 2rem;
    color: rgb(229,62,66);
    top: 131rem;
    left: 53rem;
  }
  .dibu img{
    position: absolute;
    width: 4.8rem;
    height: 4.8rem;
    top: 109rem;
    left: 65.5rem;
  }
  .jiantou img{
    position: absolute;
    width: 2.4rem;
    height: 2.6rem;
    top: 110rem;
    left: 66.5rem;

  }
</style>
