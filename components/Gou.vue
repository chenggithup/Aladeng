<template>
<div class="wrap">
<div class="cx">
  <div class="wz">
    <div><p>限时断货</p></div>
  </div>
  <img src="/static/img/huazhaungpin.png" alt="" @click="bf()">
</div>
  <div class="pinpai">
    <p>品</p>
    <p>牌</p>
    <p>精</p>
    <p>选</p>
  </div>
  <div class="chaozhi">
    超<br>
    值<br>
    热<br>
    卖<br>
  </div>
  <div class="right">
    <img src="/static/img/baobao.png" alt="" @click="da()">
  </div>
  <router-link to="/shang"><div class="xia">
    <img src="/static/img/remai.png" alt="">
  </div></router-link>
  <div class="shu"></div>
  <div class="heng"></div>

</div>
</template>

<script>
    export default {
        name: "Gou",
        methods:{
          da(){
            this.$router.push('/pinpai');
          },
          bf(){
            this.$router.push("/duanhuo");
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
    /*margin-bottom: 2rem;*/
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
  .wz div{
    position: absolute;
    background-color: rgb(229,62,66);
    width: 11.2rem;
    height: 4rem;
    left:2rem;
    top: 1.5rem;
    text-align: center;
    line-height: 4rem;
  }
  .wz p{
    color: #ffffff;
    font-size: 2.4rem;
  }
  .pinpai{
    font-size: 2.4rem;
    margin-left: 5.8rem;
    margin-top: 0.5rem;
    color: rgb(241,87,121);
}
  .chaozhi{
    font-size: 2.4rem;
    margin-left: 5.8rem;
    margin-top: 1rem;
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
