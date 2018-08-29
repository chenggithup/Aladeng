<template>
  <div id="wrap">
    <div class="nav">
      <span class="span1">阿拉灯</span>
      <input class="inp" type="text" value="" placeholder="输入商品关键字">
      <img class="sousuo" src="/static/img/sousuo.png" alt="">
      <img style="width: 3.8rem;height: 3.8rem;position: absolute;right: 2.2rem;top: 3rem;" src="/static/img/xiaoxi.png" alt="" @click="dian()">
    </div>
    <div class="nave">
      <router-link to="/shouye"><span>推荐</span></router-link>
      <router-link to="/kaishou"><span>贼惦记</span></router-link>
      <router-link to="/meishi"><span>美食</span></router-link>
      <router-link to="/muying"><span>母婴</span></router-link>
    </div>
    <Ba></Ba>
    <!--<div class="kk"></div>-->
    <Kai></Kai>
    <Kai style="margin-top: -2.5rem"></Kai>
    <div class="bm"></div>
    <div class="bottom">
      <div>
        <router-link to="/shouye"><img @click="de()" class="m1" style="width:4.8rem;height: 4.8rem;" src="/static/img/shouyeqian.png" alt=""></router-link>
        <p class="pp1">首页</p>
      </div>
      <div @click="fen()">
        <router-link to="/fenlei"><img class="i1" style="width:4.8rem;height: 4.8rem;" src="/static/img/fenleiqian.png" alt=""></router-link>
        <p>分类</p>
      </div>
      <router-link to="/dhuowang"><div>
        <img style="width:11.3rem;height: 5.5rem;" src="/static/img/duanhuo.png" alt="">
      </div></router-link>
      <router-link to="/nopur"><div>
        <img @click="mm()" class="m2" style="width: 5rem;height: 4.8rem;" src="/static/img/gouwuche.png" alt="">
        <p class="pp2">购物车</p>
      </div></router-link>
      <div>
        <router-link to="/dz"><img style="width: 4.3rem;height: 4.8rem;" src="/static/img/geren.png" alt=""></router-link>
        <p>个人中心</p>
      </div>
    </div>
  </div>

</template>

<script>
  import Ba from '@/components/Ba'
  import Kai from '@/components/Kai'
    export default {
        name: "Kaishou",
        methods:{
          dian(){
            this.$router.push("/xiaoxi");
          }
        },
        components:{
          Ba,
          Kai
        }

    }
</script>

<style scoped>
*{margin: 0;padding: 0;}
  #wrap{
    width: 100%;
    background-color: #f2f2f2;
  }
.nav{
  background-color: #e53e42;
  width: 100%;
  height: 9.6rem;
  line-height: 9.6rem;
  position: relative;
  /*border: 1px solid black;*/
}
.inp{
  width: 40rem;
  height: 5rem;
  border-radius: 1rem;
  font-size: 2.4rem;
  text-align: center;
}
.inp::-webkit-input-placeholder {
  /* placeholder颜色  */
  color: #e53e42;
  /* placeholder字体大小  */
  font-size: 2.4rem;
  /* placeholder位置  */
  text-align: center;
}
.span1{
  font-size: 3.6rem;
  color: #fff;
  position: absolute;
  left: 2.4rem;
}
.nave{
  width: 100%;
  height: 6rem;
  display: flex;
  justify-content: space-around;
  /*border: 1px solid black;*/
  line-height: 6rem;
  padding-top: 1rem;
  background-color: #fff;
}
  .nave span{
    font-size: 3rem;
  }
  .nave span:hover{
    color: #e83d41;
    border-bottom: 1px solid #ff0000;
  }
  p{
    margin-top: -8rem;
    font-size: 2rem;
  }
  .sousuo{
    width: 2.8rem;
    height: 3rem;
    position: absolute;
    left: 24.4rem;
    top: 3.3rem;
  }
  .bm{
    height: 10rem;
    background-color: #fff;
  }

.bottom{
  margin-top: 10rem;
  position: fixed;
  left: 0;
  bottom: 0;
  background-color: #fff;
  display: flex;
  justify-content: space-around;
  width: 100%;
  height: 9.7rem;
  text-align: center;
  line-height: 9.7rem;
  border-top: 1px solid #e6e6e6;
}
.bottom img{
  margin-top: 1.5rem;
}
p{
  margin-top: -8rem;
  font-size: 2rem;
  color: #666666;
}
</style>
