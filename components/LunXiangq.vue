<template>
<div v-if="bol1" class="wrap">
  <div class="pp0"></div>
  <div class="top">
    <img @click="xiulian()" src="/static/img/fanhui.png" alt="">
    <span>品牌名字</span>
    <img class="fx" @click="fenx()" src="/static/img/fenxiang.png" alt="">
  </div>

  <div class="tu">
    <img src="/static/img/lunbo.png" alt="">
    <div class="jieshao">
      <span style="text-align: left;padding-left: 1rem">Rose Hydrosed是一款来自澳大利亚的护肤产品,主要功能为深层次滋润肌肤,锁住水分,打造玫瑰般娇嫩的皮肤......</span>
        <p>下面给您推荐一些产品</p>
    </div>
  </div>

  <div class="paih">
    <div class="paih01">
    <img src="/static/img/paiming.png" alt="">
      <span style="left: 12rem;top: 2rem;">防晒类</span>   <span style="left: 24rem;top: 2rem;">第1位</span>
      <div class="x1"></div>
      <div class="x2"></div>
      <div class="x3"></div>
    </div>
    <div class="paih02">
     <div class="img"><img :src="arrA[14].src" alt=""></div>
      <span class="bao">美肤宝</span><br>
      <span class="xiaog">{{arrA[14].miaoshu}}</span>
     <button class="mai">立即购买 △</button>
    </div>
  </div>
<div class="huigu">往期上榜</div>
  <div class="tabs">
    <div class="tab" @click="toggleTab('Lxq1')">
      <span class="jx">防晒</span>
    </div>
    <div class="tab" @click="toggleTab('Lxqtwo')">
      <span class="jx">爽肤水</span>
    </div>
    <div class="tab" @click="toggleTab('Lxqsan')">
      <span class="jx">乳液X面霜</span>
      <img @click="xiala()" class="xiala" src="/static/img/xiajian.png" alt="">
    </div>
  </div>


  <div v-show="bols" class="all">
    <div class="tlt"><p>所有分类</p></div>
    <div style="margin-top: 0rem;border-top: 1px #cccccc solid" class="tabs">
      <div class="tab" @click="toggleTab('Lxq1')">
        <span class="jx">防晒</span>
      </div>
      <div class="tab" @click="toggleTab('Lxqtwo')">
        <span class="jx">爽肤水</span>
      </div>
      <div class="tab" @click="toggleTab('Lxq1')">
        <span class="jx">散装蜜粉</span>
      </div>
      <div class="tab" @click="toggleTab('Lxqtwo')">
        <span class="jx">卸妆水</span>
      </div>
      <div class="tab" @click="toggleTab('Lxqsan')">
        <span class="jx">乳液X面霜</span>
      </div>

    </div>

  </div>
  <Lxq1 :is="currentTab" keep-alive></Lxq1>
  <div class="huigu">往期上榜</div>

  <div class="paih">
    <div class="paih01">
      <img src="/static/img/paix2.png" alt="">
      <span style="left: 12rem;top: 2rem;">防晒类</span>   <span style="left: 24rem;top: 2rem;">第2位</span>
      <div class="x1"></div>
      <div class="x2"></div>
      <div class="x3"></div>
    </div>
    <div class="paih02">
      <div class="img"><img :src="arrA[14].src" alt=""></div>
      <span class="bao">美肤宝</span><br>
      <span class="xiaog">{{arrA[14].miaoshu}}</span>
      <button class="mai">立即购买 △</button>
    </div>
  </div>

  <Lxq1></Lxq1>
  <div v-show="bol" class="fenx">
    <ul>
      <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height: 6.4rem;"  src="/static/img/pengyouquan.png" alt=""><span>朋友圈</span> </a> </li>
      <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height:6.4rem;"  src="/static/img/weixin.png" alt=""><span>微信好友</span> </a> </li>
      <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height:6.4rem;"  src="/static/img/QQ.png" alt=""><span>QQ好友</span> </a> </li>
      <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height:6.4rem;"  src="/static/img/QQkongjian.png" alt=""><span>QQ空间</span> </a> </li>
      <li><a href="https://www.sina.com.cn/">   <img style="width: 6.4rem;height: 6.4rem;" src="/static/img/weibo.png" alt=""> <span>新浪微博</span> </a> </li>
      <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height: 6.4rem;"  src="/static/img/fuzhilianjie.png" alt=""><span>复制链接</span> </a> </li>

    </ul>
    <button @click="ml()">取消</button>
  </div>


</div>
</template>

<script>
  import Lxq1 from '@/components/Lxq1'
  import Lxqtwo from '@/components/Lxqtwo'
  import Lxqsan from '@/components/Lxqsan'
  import axios from 'axios'
  export default {
    name: "LunXiangq",
    data () {
      return {
        currentTab: 'Lxq1', // currentTab 用于标识当前触发的子组件
        arr:[1,2],
        bols:false,
        bol:false,
        bol1:false,
        arrA:[]
      };
    },
    components: { // 声明子组件
      Lxq1,
      Lxqtwo,
      Lxqsan
    },
    methods: {
      toggleTab: function(tab) {
        this.currentTab = tab; // tab 为当前触发标签页的组件名
      },
      xiala(){
        this.bols = !this.bols;
      },
      xiulian(){
        this.$router.push('/shouye');
      },
      fenx(){
        this.bol=!this.bol;
        document.getElementsByClassName("top")[0].style.opacity="0.1";
        document.getElementsByClassName("tu")[0].style.opacity="0.1";
        document.getElementsByClassName("paih")[0].style.opacity="0.1";
        document.getElementsByClassName("pp0")[0].style.webkitZIndex="100";

      },
      ml(){
        this.bol=!this.bol;
        document.getElementsByClassName("top")[0].style.opacity="1";
        document.getElementsByClassName("tu")[0].style.opacity="1";
        document.getElementsByClassName("paih")[0].style.opacity="1";
        document.getElementsByClassName("pp0")[0].style.webkitZIndex="-1";
      }
    },
    mounted:function () {
      axios.get('/api/phph0302/zh01.php').then((res)=>{
        this.bol1=true;
        this.arrA=res.data
      })
    }
  }
</script>

<style scoped>
  .pp0{
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100rem;
    background-color: rgba(0,0,0,0.01);
    z-index: -1;
  }
  *{margin: 0;padding: 0;}
  .wrap{width: 100%;
    background-color: #feeaf5;
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

  .tu{background-color:#feeaf5;position: relative;
    width: 100%;}
  .tu img:nth-child(1){
    width: 100%;
    height: 30.1rem;
  }
  .tu img:nth-child(2){
    width: 10rem;
    height: 10rem;
    margin-top: -3rem;
    margin-left: 2rem;
  }
  .jieshao{
    width: 100%;
    background-color: white;
    margin-top: 1.5rem;
  }
  .jieshao span{
    display: inline-block;
    font-size: 2.8rem;
    color: #4d4d4d;
    margin-top: 1.5rem;
  }
.jieshao p{
  font-size: 2.8rem;
  color: #4d4d4d;
}

.paih{
  width: 100%;background-color: white;
  margin-top: 1.5rem;
  position: relative;
}
.paih01{
  position: relative;
}
.paih01 img{
  width: 7.9rem;
  height: 9rem;
  margin-left: -60rem;
  margin-top: 1rem;

}
.img {
  width: 16rem;
  height: 18rem;
  border: 1px #cccccc solid;
  text-align: center;

}
.paih01 span{
  position: absolute;
  font-size: 2.8rem;
  color: #c46c25;
}
 .x1,.x2,.x3{
    width: 500px;
    height: 1px;
    background-color: #c46c25;
   position: absolute;
  }
  .x1{
    left: 12rem;
    top: 6rem;
  }
  .x2{
    left: 12rem;
    top: 7rem;
  }
  .x3{
    left: 12rem;
    top: 8rem;
  }
.paih02{
  margin-top: 2.6rem;
  position: relative;
  height: 18rem;
}
  .paih02 img{
    width: 13.4rem;
    height: 10.8rem;
   margin-top: 4rem;
    margin-left: 2rem;
  }
  .paih span{position: absolute;}
  .bao{
    font-size: 3rem;
    color: #4d4d4d;
    top:0rem;
    left: 17rem;
  }
  .xiaog{
    display: inline-block;
    width: 49rem;
    font-size: 2.4rem;
    color: #808080;
    top:5rem;
    left: 17rem;
  }
  .mai{
    width: 12rem;
    height: 3rem;
    background-color: #e53e42;
    font-size: 1.8rem;
    color: white;
    position: absolute;
    bottom:1rem;
    left: 17rem;
  }

  .tabs{
    width: 100%;
    height: 6rem;
    margin-top: 2rem;
    background-color: white;
    display: flex;
    justify-content: space-around;
    line-height: 6rem;
  }
  .tab{
    font-size: 2.8rem;
    color: black;
  }
  .jx:hover{
    color: red;
  }

  .huigu{
    width: 100%;
    height: 6rem;
    background-color: #e8b2d0;
    text-align: center;
    line-height: 6rem;
    font-size: 3rem;
    color: #4d4d4d;
  }
  .xiala{
    width: 2.4rem;
    height: 1.4rem;
  }
.tlt{
  width: 100%;
  height: 6rem;
  font-size: 2.8rem;
  color: #808080;
  line-height: 6rem;
  border: 1px #cccccc solid;
  background-color: white;
}
  .tlt p{
    margin-left: 2rem;
  }
  .xiaog{
    font-size: 2.4rem;
    color: #808080;
  }
  .fenx{
    width: 100%;
    height: 45rem;
    background-color: white;
    position: fixed;
    left: 0;
    bottom: 0;
    z-index: 2;
  }
  .fenx ul{
    margin-top: 2rem;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  .fenx ul li{
    font-size: 2rem;
    margin-bottom: 15px;
    display: block;
    height: 15rem;
    width: 33%;
    position: relative;
  }
  .fenx ul li span{
    font-size: 2.4rem;
    position: absolute;
    left: 8rem;
    top: 8rem;
  }
  .fenx ul li a {
    color: #555;
    display: block;
    text-decoration:none;
  }
  .fenx button{
    font-size: 2.4rem;
    width:17rem;
    height: 5.5rem;
    color:white;
    border-radius: 2rem;
    background:red;
  }

</style>
