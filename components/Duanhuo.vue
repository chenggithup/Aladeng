<template>
<div v-if="bol1" class="wrap">
  <div class="pp0"></div>
  <div class="toubu"></div>
  <div class="tt">
    <div class="zuo">
      <img src="/static/img/zuo.png" alt="" @click="be()">
    </div>
    <p class="p1">限时断货</p>
    <div class="gw">
      <img src="/static/img/gouwu.png" alt="" @click="jp()">
    </div>
    <div class="fx">
      <img src="/static/img/fenxiang.png" alt="" @click="fenx()">
    </div>
    <div class="sy">
      <img src="/static/img/shouye.png" alt="" @click="shou()">
    </div>
    <div class="baobei">
      宝贝即将售盤,再不抢就没了哦~
    </div>
    <div class="slider">
      <div class="mianbao">
        <img src="/static/img/mianbao.png" alt="">
      </div>
      <div class="zl">
        {{arr[3].names}}
      </div>
      <div class="wd">
        {{arr[3].miaoshu}}
      </div>
      <div class="pirce">
        {{arr[3].jiage}}
      </div >
      <div class="ty">
        <img src="/static/img/tuoyuan.png" alt="">
      </div>
      <div class="qing">
        马上抢
      </div>
      <div class="right">
        <img src="/static/img/you.png" alt="">
      </div>
      <div class="time"><Ds style="font-size: 1.6rem;text-align: left;"></Ds></div>
    </div>
    <div class="slider1">
      <div class="mianbao1">
        <img src="/static/img/mianbao.png" alt="">
      </div>
      <div class="zl1">
        {{arr[3].names}}
      </div>
      <div class="wd1">
        {{arr[3].miaoshu}}
      </div>
      <div class="pirce1">
        {{arr[3].jiage}}
      </div >
      <div class="ty1">
        <img src="/static/img/tuoyuan.png" alt="">
      </div>
      <div class="qing1">
        马上抢
      </div>
      <div class="right1">
        <img src="/static/img/you.png" alt="">
      </div>
      <div class="time1"><Ds style="font-size: 1.6rem;text-align: left;"></Ds></div>
    </div>
    <div class="slider2">
      <div class="mianbao2">
        <img src="/static/img/mianbao.png" alt="">
      </div>
      <div class="zl2">
        {{arr[3].names}}
      </div>
      <div class="wd2">
        {{arr[3].miaoshu}}
      </div>
      <div class="pirce2">
        {{arr[3].jiage}}
      </div >
      <div class="ty2">
        <img src="/static/img/tuoyuan.png" alt="">
      </div>
      <div class="qing2">
        马上抢
      </div>
      <div class="right2">
        <img src="/static/img/you.png" alt="">
      </div>
      <div class="time2"><Ds style="font-size: 1.6rem;text-align: left;"></Ds></div>
    </div>
    <div class="slider3">
      <div class="mianbao3">
        <img src="/static/img/mianbao.png" alt="">
      </div>
      <div class="zl3">
        {{arr[3].names}}
      </div>
      <div class="wd3">
        {{arr[3].miaoshu}}
      </div>
      <div class="pirce3">
        {{arr[3].jiage}}
      </div >
      <div class="ty3">
        <img src="/static/img/tuoyuan.png" alt="">
      </div>
      <div class="qing3">
        马上抢
      </div>
      <div class="right3">
        <img src="/static/img/you.png" alt="">
      </div>
      <div class="time3"><Ds style="font-size: 1.6rem;text-align: left;"></Ds></div>
    </div>
  </div>

  <div class="tu"><img src="/static/img/dingbu.png" alt="" @click="dingbu()"></div>
  <div v-show="bols" class="fenx">
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
    import Ds from '@/components/Ds'
    import axios from 'axios'
    export default {
        name: "Duanhuo",
      data(){
        return{
          arr:[],
          bols:false,
          bol1:false
        }
      },
        methods:{
          be(){
            this.$router.push('/shouye');
          },
          dingbu(){
            $('html,body').animate({scrollTop:0},'slow');
          },
          fenx(){
            this.bols=true;
            document.getElementsByClassName("tt")[0].style.opacity="0.1";
            document.getElementsByClassName("pp0")[0].style.zIndex="100";

          },
          ml(){
            this.bols=!this.bols;
            document.getElementsByClassName("tt")[0].style.opacity="1";
            document.getElementsByClassName("pp0")[0].style.zIndex="-1";
          },
          shou(){
            this.$router.push('/shouye');
          },
          jp(){
            this.$router.push('/gouwu');
          }
        },
      components:{
          Ds
      },
      mounted:function () {
        axios.get("/api/phph0302/zh01.php").then((res)=>{
          this.arr=res.data;
          console.log(this.arr);
          this.bol1=true;
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
    height: 63rem;
    background-color: rgba(0,0,0,0.01);
    z-index: -1;
  }
  .wrap{
    margin: 0;
    padding: 0;
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
    top: 4rem;
    width: 2.3rem;
    height: 3.8rem;
  }
  .p1{
    position: absolute;
    font-size: 3.6rem;
    color: white;
    left: 27rem;
    top: 3.5rem;
  }
  .gw img{
    position: absolute;
    width: 3.6rem;
    height: 3.4rem;
    top: 4.5rem;
    left: 55rem;
  }
  .fx img{
    position: absolute;
    width: 3.6rem;
    height: 3.4rem;
    top: 4.5rem;
    left: 61rem;

  }
  .sy img{
    position: absolute;
    width: 3.6rem;
    height: 3.6rem;
    top: 4.5rem;
    left: 66rem;
  }
  .baobei{
    position: absolute;
     font-size: 3rem;
    top:11.5rem;
    left: 1rem;
    color: rgb(77,77,77);
  }
  .slider{
    position: relative;
    border: 1px solid rgb(204,204,204) ;
    top: 17.5rem;
    width: 72rem;
    height: 20rem;
  }
  .mianbao img{
    position: absolute;
    width: 18rem;
    height: 16rem;
    top: 2rem;
    left: 1rem;
  }
  .zl{
    position: absolute;
    font-size: 3rem;
    top: 1.5rem;
    left:20rem;
  }
  .wd{
    position: absolute;
    font-size: 2.4rem;
    left: 20rem;
    top: 7rem;
  }
 .pirce{
   position: absolute;
   font-size: 2.8rem;
   color: rgb(229,62,66);
   left: 20rem;
   top: 12rem;
 }
  .ty img{
    position: absolute;
    width: 12rem;
    height: 4rem;
    top: 12rem;
    left: 57.5rem;
  }
  .qing{
    position: absolute;
    font-size: 1.8rem;
    top: 12.5rem;
    left: 59.5rem;
    color: rgb(255,255,255);
  }
  .right img{
    position: absolute;
    width: 1.1rem;
    height: 1.8rem;
    top: 13rem;
    left: 67rem;
  }
  .time{
    position: absolute;
    font-size: 1.6rem;
    color: rgb(229,62,66);
    top: 17rem;
    left: 58rem;
  }
  .slider1{
     position: relative;
     border: 1px solid rgb(204,204,204) ;
     top: 17.5rem;
     width: 72rem;
     height: 20rem;
   }
  .mianbao1 img{
    position: absolute;
    width: 18rem;
    height: 16rem;
    top: 2rem;
    left: 1rem;
  }
  .zl1{
    position: absolute;
    font-size: 3rem;
    top: 1.5rem;
    left:20rem;
  }
  .wd1{
    position: absolute;
    font-size: 2.4rem;
    left: 20rem;
    top: 7rem;
  }
  .pirce1{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(229,62,66);
    left: 20rem;
    top: 12rem;
  }
  .ty1 img{
    position: absolute;
    width: 12rem;
    height: 4rem;
    top: 12rem;
    left: 57.5rem;
  }
  .qing1{
    position: absolute;
    font-size: 1.8rem;
    top: 12.5rem;
    left: 59.5rem;
    color: rgb(255,255,255);
  }
  .right1 img{
    position: absolute;
    width: 1.1rem;
    height: 1.8rem;
    top: 13rem;
    left: 67rem;
  }
  .time1{
    position: absolute;
    font-size: 1.6rem;
    color: rgb(229,62,66);
    top: 17rem;
    left: 58rem;
  }
  .slider2{
    position: relative;
    border: 1px solid rgb(204,204,204) ;
    top: 17.5rem;
    width: 72rem;
    height: 20rem;
  }
  .mianbao2 img{
    position: absolute;
    width: 18rem;
    height: 16rem;
    top: 2rem;
    left: 1rem;
  }
  .zl2{
    position: absolute;
    font-size: 3rem;
    top: 1.5rem;
    left:20rem;
  }
  .wd2{
    position: absolute;
    font-size: 2.4rem;
    left: 20rem;
    top: 7rem;
  }
  .pirce2{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(229,62,66);
    left: 20rem;
    top: 12rem;
  }
  .ty2 img{
    position: absolute;
    width: 12rem;
    height: 4rem;
    top: 12rem;
    left: 57.5rem;
  }
  .qing2{
    position: absolute;
    font-size: 1.8rem;
    top: 12.5rem;
    left: 59.5rem;
    color: rgb(255,255,255);
  }
  .right2 img{
    position: absolute;
    width: 1.1rem;
    height: 1.8rem;
    top: 13rem;
    left: 67rem;
  }
  .time2{
    position: absolute;
    font-size: 1.6rem;
    color: rgb(229,62,66);
    top: 17rem;
    left: 58rem;
  }
  .slider3{
    position: relative;
    border: 1px solid rgb(204,204,204) ;
    top: 17.5rem;
    width: 72rem;
    height: 20rem;
  }
  .mianbao3 img{
    position: absolute;
    width: 18rem;
    height: 16rem;
    top: 2rem;
    left: 1rem;
  }
  .zl3{
    position: absolute;
    font-size: 3rem;
    top: 1.5rem;
    left:20rem;
  }
  .wd3{
    position: absolute;
    font-size: 2.4rem;
    left: 20rem;
    top: 7rem;
  }
  .pirce3{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(229,62,66);
    left: 20rem;
    top: 12rem;
  }
  .ty3 img{
    position: absolute;
    width: 12rem;
    height: 4rem;
    top: 12rem;
    left: 57.5rem;
  }
  .qing3{
    position: absolute;
    font-size: 1.8rem;
    top: 12.5rem;
    left: 59.5rem;
    color: rgb(255,255,255);
  }
  .right3 img{
    position: absolute;
    width: 1.1rem;
    height: 1.8rem;
    top: 13rem;
    left: 67rem;
  }
  .time3{
    position: absolute;
    font-size: 1.6rem;
    color: rgb(229,62,66);
    top: 17rem;
    left: 58rem;
  }

  .tu{
    position: fixed;
    right: 0;
    bottom: 20rem;
  }
  .tu img{
    width: 4.8rem;
    height: 4.8rem;
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
