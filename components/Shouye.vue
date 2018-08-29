<template>
    <div class="wrap">
      <div class="nav">
        <span class="span1">阿拉灯</span>
        <input class="inp" type="text" value="" placeholder="输入商品关键字" @click="dj()">
        <img class="sousuo" src="/static/img/sousuo.png" alt="">
        <img style="width: 3.8rem;height: 3.8rem;position: absolute;right: 2.2rem;top: 3rem;" src="/static/img/xiaoxi.png" alt="" @click="dian()">
      </div>
      <div class="nave">
        <router-link to="/shouye"><span>推荐</span></router-link>
        <router-link to="/kaishou"><span>贼惦记</span></router-link>
        <router-link to="/meishi"><span>美食</span></router-link>
        <router-link to="/muying"><span>母婴</span></router-link>
      </div>
      <lunbo></lunbo>
      <div class="xinpin"><img src="/static/img/laba.png" alt=""><span>新品上市 促销大庆</span></div>
      <gou></gou>
      <div class="xinpin"><img class="img" src="/static/img/tuijian.png" alt=""><span>今日推荐</span></div>
      <tui></tui>
      <tui></tui>
      <div class="kk"></div>
      <div class="bottom">
      <div>
        <router-link to="/shouye"><img @click="de()" class="m1" style="width:4.8rem;height: 4.8rem;" src="/static/img/shouyeqian.png" alt=""></router-link>
        <p class="pp1">首页</p>
      </div>
      <div>
        <router-link to="/fenlei"><img class="i1" style="width:4.8rem;height: 4.8rem;" src="/static/img/fenleiqian.png" alt=""></router-link>
        <p>分类</p>
      </div>
      <router-link to="/dhuowang"><div>
        <img style="width:11.3rem;height: 5.5rem;" src="/static/img/duanhuo.png" alt="">
      </div></router-link>
      <router-link to="/gouwu"><div>
        <img class="m2" style="width: 5rem;height: 4.8rem;" src="/static/img/gouwuche.png" alt="">
        <p class="pp2">购物车</p>
      </div></router-link>
      <div>
        <router-link to="dz"><img style="width: 4.3rem;height: 4.8rem;" src="/static/img/geren.png" alt=""></router-link>
        <p>个人中心</p>
      </div>
    </div>
    </div>
</template>

<script>
    import Lunbo from '@/components/Lunbo'
    import Tui from '@/components/Tui'
    import Gou from '@/components/Gou'
    export default {
        name: "Shouye",
        data(){
          return{
            n:0
          }
        },
        components:{
          Lunbo,
          Tui,
          Gou
        },
        methods:{
          fen(){
            this.$router.push("/fenlei");
          },
          dian(){
            this.$router.push("/xiaoxi");
          },
          dj(){
            this.$router.push("/sousuo");
          },
          de(){
            this.n++;
            if(this.n % 2 ==0){
              document.getElementsByClassName("m1")[0].src="/static/img/shouyeqian.png";
              document.getElementsByClassName("pp1")[0].style.color= '';
            }else{
              document.getElementsByClassName("m1")[0].src="/static/img/shouyehou.png";
              document.getElementsByClassName("pp1")[0].style.color= '#f00';
            }
          }
        }
    }
</script>

<style scoped>
  .wrap{
    width: 100%;
    background-color: #f2f2f2;
    overflow-y: scroll;
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
    border-bottom: 0.2rem solid #ff0000;
  }
  .xinpin{
    margin-top: 2rem;
    margin-left: -40rem;
    font-size: 3rem;
    height: 6rem;
    line-height: 6rem;
    background-color: #fff;
    padding-top: 1rem;
    padding-bottom: 1rem;
  }
  .xinpin img{
    width: 3rem;
    height: 3rem;
    vertical-align: center;
  }
  .xinpin span{
    font-size: 3rem;
    margin-left: 1rem;
  }
  .img{
    margin-left: -13rem;
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
  .sousuo{
    width: 2.8rem;
    height: 3rem;
    position: absolute;
    left: 24.4rem;
    top: 3.3rem;
  }
  .kk{
    margin-bottom: 6rem;
  }

</style>
