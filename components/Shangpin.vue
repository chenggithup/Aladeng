<template>
  <div v-if="bol" class="wrap">
    <div class="toubu"></div>
    <div class="zjt">
      <router-link to="/koured"><img src="/static/img/zuo.png" alt=""></router-link>
    </div>
    <p class="xq">商品详情</p>
    <div class="fx">
      <img src="/static/img/fenxiang.png" alt="">
    </div>
    <div class="one">
      <img :src="arr[0].src" alt="">
    </div>
    <div class="two">
      <img :src="arr[0].src" alt="">
    </div>
    <div class="three">
      <img :src="arr[0].src" alt="">
    </div>
    <div class="four">
      <img :src="arr[0].src" alt="">
    </div>
    <div class="five">
      <img :src="arr[0].src" alt="">
    </div>
    <div class="six">
      <img :src="arr[0].src" alt="">
    </div>
    <div class="slider">
       <div class="music">
         <img src="/static/img/erji.png" alt="">
       </div>
      <div class="kefu">
        在线客服
      </div>
    </div>
    <div class="slider1">
       <div @click="mai()" class="gouwu">加入购物车</div>
    </div>

  </div>
</template>

<script>
    import axios from 'axios'
    export default {
        name: "Shangpin",
        data(){
          return{
            bol:false,
            arr:[]
          }
        },
      mounted: function () {
        axios.get('/api/phph0302/zh01.php').then((res)=>{
          this.bol=true;
          this.arr=res.data
        })
      },
      methods:{
        mai(){
          this.$router.push("/gouwu");
        }
      }
    }
</script>

<style scoped>
.wrap{
  margin: 0;
  padding: 0;
  position: relative;
  width: 100%;
  background-color: #f2f2f2;
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
.xq{
  position: absolute;
  font-size: 3.6rem;
  color: white;
  left: 27rem;
  top: 3.5rem;
}
.fx img{
  position: absolute;
  width: 3.6rem;
  height: 3.4rem;
  top: 4.5rem;
  left: 63rem;
}
  .one img{
    position: absolute;
    width: 12rem;
    height: 24.5rem;
    top: 20rem;
    left: 30rem;
  }
  .two img{
    position: absolute;
    width: 12rem;
    height: 24.5rem;
    top: 60rem;
    left: 30rem;
  }
 .three img{
   position: absolute;
   width: 12rem;
   height: 24.5rem;
   top: 100rem;
   left: 30rem;
 }
.four img{
  position: absolute;
  width: 12rem;
  height: 24.5rem;
  top: 140rem;
  left: 30rem;
}
.five img{
  position: absolute;
  width: 12rem;
  height: 24.5rem;
  top: 180rem;
  left: 30rem;
}
.six img{
  position: absolute;
  width: 12rem;
  height: 24.5rem;
  top: 220rem;
  left: 30rem;
}
  .slider{
    position: absolute;

    width: 36rem;
    height: 9.5rem;
    top: 255rem;
    background-color: whitesmoke;
  }
  .music img{
    position: absolute;
    width: 3.7rem;
    height: 3rem;
    top: 4rem;
    left: 8rem;
  }
  .kefu{
    position: absolute;
    font-size: 2.8rem;
    color:rgb(77,77,77);
    font-family: SimHei;
    top: 3.5rem;
    left: 13rem;
  }
.slider1{
  position: absolute;
  border: 1px solid rgb(229,62,66);
  width: 36rem;
  height: 9.5rem;
  background-color: rgb(229,62,66);
  top: 255rem;
  left: 36rem;
}
  .gouwu{
    position: absolute;
    font-size: 2.8rem;
    font-family: SimHei;
    color:rgb(255,255,255) ;
    top: 3rem;
    left: 11rem;
  }
</style>
