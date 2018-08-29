<template>
  <div class="wrap">
    <div class="cx">
      <div class="wz">
        <div><p>GO</p></div>
        <span>闭关修炼</span>
      </div>
      <img src="/static/img/huazhaungpin.png" alt="" @click="bb()">
    </div>
    <div class="pinpai">

      <div><p>GO</p></div>
      <span>超逼格</span>
    </div>
    <div class="chaozhi">
    <div style="left: 0;top: 4rem"><p>GO</p></div>
      <span>必买清单</span>
    </div>
    <div class="right">
      <img src="/static/img/baobao.png" alt="">
    </div>
    <div class="xia">
      <router-link to="/bibai"><img src="/static/img/remai.png" alt=""></router-link>
    </div>
    <div class="shu"></div>
    <div class="heng"></div>

  </div>
</template>

<script>
  export default {
    name: "Ba",
    methods:{
      bb(){
        this.$router.push("/xiulian")
      }
    }
  }
</script>


<style scoped>
  .wrap{
    width: 100%;
    height: 30rem;
    position: relative;
    background-color: #fff;
    border-bottom: 1px #c2c2c2 solid;
  }
  .cx img{
    position: absolute;
    width: 24.1rem;
    height: 19.5rem;
    left: 4rem;
    top: 8.2rem;
  }
  .wz{
    border-top: 1px solid #c2c2c2;
    border-bottom: 1px solid #c2c2c2;
  }
  .wz div,.pinpai div,.chaozhi div{
    position: absolute;
    background-color: rgb(229,62,66);
    width: 6.4rem;
    height: 4.3rem;
    left:2rem;
    top: 6rem;
    text-align: center;
    line-height: 4rem;
  }
  .wz p,.pinpai p,.chaozhi p{
    color: white;
    font-size: 2.4rem;
  }
  .pinpai div{
    top: 4rem;
    left:0rem;
  }

  .wz span{
    position: absolute;
    left:2rem;
    top: 2rem;
    color: #e96466;
    font-size: 2.4rem;
  }
  .pinpai{
    font-size: 2.4rem;
    margin-top: 0.5rem;
    color: rgb(241,87,121);
    position: absolute;
    right: 32rem;
  }
  .chaozhi{
    font-size: 2.4rem;
    position: absolute;
    right: 29rem;
   top: 15rem;
    color: rgb(241,87,121);
  }
  .right img{
    position: absolute;
    width: 20rem;
    height: 12rem;
    left: 45rem;
    top: 2rem;
  }
  .xia img{
    position: absolute;
    width: 20rem;
    height: 12rem;
    left: 45.5rem;
    top: 16rem;
  }
  .shu{
    position: absolute;
    width: 0.1rem;
    height: 27rem;
    left: 31.2rem;
    top: 1rem;
    background-color: #c2c2c2;
  }
  .heng{
    position: absolute;
    width: 39.8rem;
    height: 0.1rem;
    background-color:#c2c2c2;
    left: 31.7rem;
    top: 14.6rem;
  }

</style>
