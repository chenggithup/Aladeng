<template>
   <div v-if="bol" id="wrap">
     <div class="top">
       <img @click="xiulian()" src="/static/img/fanhui.png" alt="">
       <span>女神汉纸到女神的脱变</span>
       <img class="fx" src="/static/img/fenxiang.png" alt="">
     </div>
     <div class="nvs">
       <img src="/static/img/nvshen.png" alt="">
       <img src="/static/img/beij03.png" alt="">
       <div class="shenj">
         <div></div>
         <span> 女 神 → 女 汉 子 差 不 是 一 两 步</span>
       </div>
       <h1>ADDICTION</h1>
           <h5>BY  AYAKO</h5>

       <span class="sps1">ADDICTION专为z追求自我风格的各年龄层女性而设,</span><br>
       <span style="font-size: 2.8rem;color: #333333">由NARS的前彩妆总监Ayako掌舵</span><br>
       <span class="sps1">质感奢华,宛如定制</span><br>
       <span class="sps1">上市以来已获得35项彩妆奖项,</span><br>
       <span class="sps1">是日本杂志和化妆师力荐品牌</span>
     </div>

     <div class="cont">
       <img src="/static/img/yanying02.png" alt="">
       <img src="/static/img/yanying.png" alt="">

       <div class="miaoshu">
         <span style="color: red;font-size: 3rem;">ADDICTION单色眼影@cosme 2016综合大赏、2016眼影部门第一位。</span>
         <span style="color: #4d4d4d;font-size: 2.8rem;">一直是超热产品,色卡团简直是看得人眼花缭乱,但是却没有一款是多余的。色彩饱和度高,易上色,在肌肤上显色鲜亮饱满。粉质软弱易晕染,颜色均匀不结块。可以自由组合配色处化眼影的人参考官网的专业配色也可以轻松驾驭</span>

       </div>
     </div>

     <div class="db">
       <img class="dingbu" style=" width: 4.8rem;
    height: 4.8rem;" src="/static/img/dingbu.png" @click="dingbu()" alt=""><h1>返回顶部</h1>
     </div>

     <div style="background-color: white;margin-top: 0rem" class="cont">
       <img style="margin-top: 1.5rem" src="/static/img/kouhong2.png" alt="">
       <img src="/static/img/yanying.png" alt="">

       <div class="miaoshu">
         <span style="color: red;font-size: 3rem;">ADDICTION单色眼影@cosme 2016综合大赏、2016眼影部门第一位。</span>
         <span style="color: #4d4d4d;font-size: 2.8rem;">一直是超热产品,色卡团简直是看得人眼花缭乱,但是却没有一款是多余的。色彩饱和度高,易上色,在肌肤上显色鲜亮饱满。粉质软弱易晕染,颜色均匀不结块。可以自由组合配色处化眼影的人参考官网的专业配色也可以轻松驾驭</span>

       </div>
     </div>

     <div class="db">
     </div>

     <div class="jiage">
       <div style="border-bottom: 1px grey solid;" class="yanying">
       <img :src="arr[12].src" alt="">
       <span style="top: 1.5rem;left: 22rem">{{arr[12].names}}</span> <span style="top: 1.5rem;left: 40rem">{{arr[12].miaoshu}}</span>
       <span style="top: 13rem;left: 22rem;color: red;">{{arr[12].jiage}}</span>        <button @click="liji()">立即购买</button>
       </div>
       <div class="yanying">
         <img :src="arr[13].src" alt="">
         <span style="top: 1.5rem;left: 22rem">{{arr[13].names}}</span> <span style="top: 1.5rem;left: 40rem">{{arr[13].miaoshu}}</span>
         <span style="top: 13rem;left: 22rem;color: red;">{{arr[13].jiage}}</span>        <button @click="liji()">立即购买</button>
       </div>
     </div>
    <div class="gengduo">
      <p @click="gengduo()">加载更多</p>
    </div>
   </div>
</template>

<script>
    import axios from 'axios'
    export default {
        name: "goddess",
        data(){
          return{
            bol:false,
            arr:[]
          }
        },
      methods:{
        xiulian(){
          this.$router.push('/Xiulian');
        },
        dingbu(){
          $('html,body').animate({scrollTop:0},'slow');
        },
        gengduo(){
          alert("不好意思,没有更多商品了!!!!!");
        },
        liji(){
          this.$router.push('/gouwu');
        }
      },
      mounted:function () {
        axios.get('/api/phph0302/zh01.php').then((res)=>{
          this.bol = true;
          this.arr = res.data;
        })
      }
    }
</script>

<style scoped>
  *{margin: 0;padding: 0;}
  #wrap{width: 100%;background: #f2f2f2;
    height: 100%;}
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
  .nvs{position: relative;text-align: center;background-color: white;}
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
    font-size: 4.8rem;
    color: #4d4d4d;
    margin-top: 6.3rem;
  }
  .nvs h5{
    font-size: 1.6rem;
    color: #8a8a8a;
  }
  .sps1{
  font-size: 2.8rem;color: #4d4d4d;
  }
.cont{
  margin-top: 5rem;
  background-color: white;
  text-align: center;
  height: 75.6rem;
}
  .cont img:nth-child(1){
     width: 68rem;
     height: 41.1rem;
    margin-top: 1rem;
   }
  .cont img:nth-child(2){
    width: 68rem;
    height: 8rem;
    margin-top: -2rem;
  }
  .miaoshu{
    background: #f2f2f2;
    width: 64.6rem;
    height: 26rem;
    text-align: center;
    border-radius:5% ;
    margin-left: 4rem;

  }
  .db{background:#f2f2f2;margin-top: 2rem;position: relative;
    width: 100%;
    height: 2.2rem;}
  .dingbu{
    position: absolute;
    right: 3rem;
    top: -8rem;
  }
  .db h1{
    font-size:2.4rem;
    position: absolute;
    right: 0;
    color: red;
    top: -1rem;
  }
  .jiage{
    background-color: white;
    height: 40rem;
  }
  .yanying{
    width: 100%;
    height: 20.2rem;
    position: relative;
  }
  .yanying img{
    width: 18.1rem;
    height: 16.2rem;
    margin-left: -50rem;
    margin-top: 2rem;

  }
  .yanying span{font-size: 2.8rem;position: absolute;}
  .yanying button{
    font-size: 1.9rem;
    text-align: center;
    line-height: 1.8rem;
    width: 12.1rem;
    height: 4.4rem;
    border-radius: 2rem;
    color: white;
    background-color: red;
    position: absolute;
    right: 3rem;
    top: 13rem;
  }
  .gengduo{
    width: 100%;
    height: 10rem;
    background-color:#f2f2f2 ;
    text-align: center;
    line-height: 8rem;
    font-size: 2.4rem;
    color: #808080;
  }



</style>
