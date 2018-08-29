<template>
  <div class="wrap">
    <div class="toubu"></div>
    <div class="zuo">
      <router-link to="/geren"><img src="/static/img/zuo.png" alt=""></router-link>
    </div>
    <p class="p1">收货地址</p>
    <router-link to="/add2"><p class="p2">添加新地址</p></router-link>
    <div class="map">
      <img src="/static/img/ditu.png" alt="">
    </div>
    <div class="new">
     <button class="btn" @click="di()">添加新地址</button>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Address",
        methods:{
          di(){
            this.$router.push("/add2")
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
  .p2{
    position: absolute;
    font-size: 3rem;
    color: white;
    left: 55rem;
    top: 3rem;
  }
  .map img{
    position: absolute;
    width: 20rem;
    height: 20rem;
    top: 30rem;
    left: 25rem;
  }
  .new button{
    position: absolute;
    width: 24rem;
    height: 6rem;
    background-color:rgb(255,255,255);
    border:2px solid rgb(77,77,77) ;
    border-radius: 25rem;
    top: 55rem;
    left: 23rem;
  }
  .btn{
   font-size: 3rem;
    color:rgb(77,77,77) ;
  }
</style>
