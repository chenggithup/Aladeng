<template>
<div id="wrap">
  <div class="top">
    <img @click="ba()" src="/static/img/fanhui.png" alt="">
    <span>修炼秘籍</span>
    <img class="fx" src="/static/img/fenxiang.png" alt="">
  </div>
 <div class="nvs">
   <img @click="xiangxi()" src="/static/img/nvshen.png" alt="">
   <img src="/static/img/beij03.png" alt="">
   <div class="shenj">
   <div></div>
<span> 女 神 → 女 汉 子 差 不 是 一 两 步</span>
   </div>
  <h1>ADDICTION</h1>
   <p>质感奢华 宛如定制</p>
 </div>

  <div class="xian"></div>

  <div class="nvs">
    <img @click="xiangxi()" src="/static/img/nvshen.png" alt="">
    <img src="/static/img/beij03.png" alt="">
    <img src="/static/img/nvshen02.png" alt="">
    <div class="shenj">
      <div></div>
      <span> 女 神 → 女 汉 子 差 不 是 一 两 步</span>
    </div>
    <h1>ADDICTION</h1>
    <p>质感奢华 宛如定制</p>
  </div>


<div class="xian"></div>

  <div class="nvs">
    <img @click="xiangxi()" src="/static/img/nvshen.png" alt="">
    <img src="/static/img/beij03.png" alt="">
    <img src="/static/img/nvshen02.png" alt="">
    <img class="dingbu" style=" width: 4.8rem;
    height: 4.8rem;" src="/static/img/dingbu.png" @click="dingbu()" alt="">

    <div class="shenj">
      <div></div>
      <span> 女 神 → 女 汉 子 差 不 是 一 两 步</span>
    </div>
    <h1>ADDICTION</h1>
    <p>质感奢华 宛如定制</p>
  </div>

  <div class="xian2">
    <p @click="noduo()">加载更多</p>
  </div>
</div>

</template>

<script>
    export default {
        name: "Xiulian",
      methods:{
        dingbu(){
          $('html,body').animate({scrollTop:0},'slow');
        },
        noduo(){
          alert("不好意思,没有更多了");
        },
        xiangxi(){
         this.$router.push('/Goddess')
        },
        ba(){
          this.$router.push('/Kaishou')
        }
      }
    }
</script>

<style scoped>
  *{margin: 0;padding: 0;}
  #wrap{width: 100%;}
  .top{display: flex;justify-content:space-between;background-color: red;
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
  .top span{font-size: 3.6rem;margin-top: 3.7rem;color: white;}
  .nvs{position: relative;}
.nvs img{
  width: 100%;
  height: 40rem;
}
  .nvs img:nth-child(2){
    width: 31.2rem;
    height: 7.8rem;
    position: absolute;
    right: 2.2rem;
    top: 18.3rem;
    z-index: 1;
  }
  .nvs img:nth-child(3){
    width: 25.6rem;
    height: 19rem;
    position: absolute;
    top: 14.4rem;
    right: 2rem;

  }
.shenj{
  width: 70rem;
  height: 8.3rem;
  background-color: white;
  position: relative;
  margin-top: -11.5rem;
  margin-left: 2rem;

}
  .shenj div{
    position: absolute;
    left: 0;
    top: 2.8rem;
    width: 0.5rem;
    height: 3rem;
    background-color: red;
  }
.shenj span{
  font-size: 3rem;
  line-height: 8.3rem;
  margin-left: 5rem;
  color: #4d4d4d;
}
  .nvs h1{
    font-size: 3rem;
    color: #333333;
    margin-top: 5rem;
    margin-left: 2rem;
  }
  .nvs p{
    font-size: 2.4rem;
    color: #717171;
    margin-left: 2rem;
    margin-top: 2rem;
  }

  .xian{
    width: 100%;
    height: 3rem;
    border-top: 1px #cccccc solid;
    margin-top:2rem;
  }
.xian2{
  margin-top: 2rem;
  width: 100%;
  height: 10rem;
  border-top: 1px #cccccc solid;
}
  .xian2{
    font-size: 2.4rem;
    line-height: 10rem;
    text-align: center;
    color: #a7a7a7;
  }
  .dingbu{
    position: absolute;
    right: 5rem;
    top: 10rem;
  }
</style>
