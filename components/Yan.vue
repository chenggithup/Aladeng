<template>
  <div class="wrap">
    <div class="top">
      <img @click="ba()" src="/static/img/fanhui.png" alt="">
      <span>绚丽眼妆</span>
      <img class="fx" src="/static/img/fenxiang.png" alt="">
    </div>
    <div class="cc">
      <img src="/static/img/xuanli.png" alt="">
    </div>
    <div class="cd">
      <div>
        <span>防晒必备</span>
      </div>
      <div>
        <span>随身面膜</span>
      </div>
      <div>
        <span>分瓶装</span>
      </div>
      <div>
        <span>化妆水<img src="/static/img/xiajian.png" alt=""></span>
      </div>
    </div>
    <div class="cf">
      <img src="/static/img/zuxing.png" alt="">
      <span>防晒必备</span>
      <img src="/static/img/zuxing.png" alt="">
    </div>
    <Naifen></Naifen>
    <div class="cf">
      <img src="/static/img/zuxing.png" alt="">
      <span>随身面膜</span>
      <img src="/static/img/zuxing.png" alt="">
    </div>
    <Naifen></Naifen>
    <div class="tu"><img src="/static/img/dingbu.png" alt="" @click="dingbu()"></div>
  </div>
</template>

<script>

    import Naifen from '@/components/Naifen'
    export default {
        name: "Yan",
        methods:{
          ba(){
            this.$router.push("/dhuowang");
          },
          dingbu(){
            $('html,body').animate({scrollTop:0},'slow');
          }
        },
        components:{
          Naifen
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
  }
  .top{
    display: flex;
    justify-content:space-between;
    background-color: red;
    height: 11.3rem;
    width: 100%;
  }
  .top img:nth-child(1){
    width: 2.3rem;
    height: 3.8rem;
    margin-top:3.7rem;
    margin-left: 2rem;
  }
  .fx{
    width: 3.6rem;
    height: 3.4rem;
    margin-top:3.7rem;
    margin-right: 2rem;
  }
  .top span{
    font-size: 3.6rem;
    margin-top: 3.7rem;
    color: white;
  }
  .cc img{
    width: 100%;
  }
  .cd{
    margin-top: 2rem;
    display: flex;
    justify-content: space-around;
    background-color: #fff;
    height: 6rem;
    line-height: 6rem;
  }
  .cd div{
    border-right: 0.1rem solid #000;
  }
  .cd span{
    font-size: 3rem;

    margin-right: 3rem;
  }
  .cd span:hover{
    color:#f00;
    border-bottom: 0.1rem solid #f00;
  }
  .cd div:nth-child(1) span{
    margin-left: 4rem;
  }
  .cd div:nth-child(4){
    border-right: 0;
  }
  .cd div:nth-child(4) span img{
    width: 2.5rem;
    height: 1.4rem;
  }
  .cf{
    margin-top: 2rem;
  }
  .cf img:first-child{
    width: 26.3rem;
    height: 2.8rem;
    margin-left: -30rem;
  }
  .cf span{
    font-size: 3rem;
    padding-left: 1rem;
    padding-right: 1rem;
    vertical-align: top;
  }
  .cf img:last-child{
    width: 26.3rem;
    height: 2.8rem;
    margin-right: -30rem;
  }
  .tu{
    position: fixed;
    right: 0;
    bottom: 0;
  }
  .tu img{
    width: 4.8rem;
    height: 4.8rem;
  }
</style>
