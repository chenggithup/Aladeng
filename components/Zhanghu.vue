<template>
    <div class="wrap">
      <div class="toubu">
      </div>
      <div class="zuo">
        <router-link to="/geren"><img src="/static/img/zuo.png" alt=""></router-link>
      </div>
      <p class="p1">我的账户</p>
        <div class="zs">
          <img src="/static/img/zuanshi.png" alt="">
        </div>
      <div class="money">
        <p>¥ 2000</p>
      </div>
      <div class="je">
        我的金额
      </div>
       <div class="tx">
          <div class="ww">
            <p @click="tixian()">提现</p>
          </div>
       </div>
</div>
</template>

<script>
    export default {
        name: "Zhanghu",
        methods:{
          tixian(){
            $(".money p").html("¥ 0.00");
            alert("提现成功!");
          }
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
  .zs img{
    position: absolute;
    width: 20.4rem;
    height: 15.2rem;
    left: 25rem;
    top: 15rem;
  }
  .money{
    position: absolute;
    font-size: 3rem;
    color: rgb(229,62,66);
    top: 33rem;
    left: 30rem;
  }
  .je{
    position: absolute;
    font-size: 3rem;
    top: 38rem;
    left: 29rem;
    color:rgb(77,77,77);
  }
  .tx{
    position: absolute;
    width: 48rem;
    height: 7.2rem;
    border: 1px solid rgb(97,167,234) ;
    background-color: rgb(97,167,234) ;
    top: 50rem;
    left: 12rem;
  }
  .ww{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(255,255,255);
    top: 1.5rem;
    left: 21rem;
  }
</style>
