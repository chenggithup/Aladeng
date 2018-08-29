<template>
<div class="wrap">
  <img class="fx" @click="fenx()" src="/static/img/fenxiang.png" alt="">
<div v-show="bols" class="fenx">
  <ul>
    <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height: 6.4rem;"  src="/static/img/pengyouquan.png" alt=""><span>朋友圈</span> </a> </li>
    <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height:6.4rem;"  src="/static/img/weixin.png" alt=""><span>微信好友</span> </a> </li>
    <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height:6.4rem;"  src="/static/img/QQ.png" alt=""><span>QQ好友</span> </a> </li>
    <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height:6.4rem;"  src="/static/img/QQkongjian.png" alt=""><span>QQ空间</span> </a> </li>
    <li><a href="https://www.sina.com.cn/">   <img style="width: 6.4rem;height: 6.4rem;" src="/static/img/weibo.png" alt=""> <span>新浪微博</span> </a> </li>
    <li><a href="https://www.sina.com.cn/">  <img style="width: 6.4rem;height: 6.4rem;"  src="/static/img/fuzhilianjie.png" alt=""><span>复制链接</span> </a> </li>

  </ul>
  <button>取消</button>
</div>



</div>
</template>

<script>
  // import $ from 'jquery'
    export default {
        name: "FenXiang",
      data(){
        return{
          bols:false,
          title:'奶粉'
        }
      },
      methods:{
       fenx(){
         this.bols=!this.bols;

       }
      }
    }
</script>

<style scoped>
  * {
    padding: 0;
    margin: 0;
  }
 .wrap {
   width: 100%;
   background-color: #f2f2f2;
 }

  .fx{
    width: 3.6rem;
    height: 3.4rem;
    margin-top:3.7rem;
    margin-right: 2rem;
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
