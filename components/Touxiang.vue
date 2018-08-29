<template>
    <div class="wrap">
      <div class="toubu">
      </div>
      <div class="zuo">
        <router-link to="/grxx"><img src="/static/img/zuo.png" alt=""></router-link>
      </div>
      <p class="p1">头像</p>
      <div class="dd">
        <img src="/static/img/gengduo.png" alt="" @click="dl()">
      </div>
     <div class="center">
       <div class="dayuan">
         <div class="tp">
           <img src="/static/img/11.jpg" alt="">
         </div>
       </div>
     </div>

      <div class="bottom" v-show="bol">
        <ul class="ul1">
          <li>从手机相册中选择</li>
          <li>拍照</li>
          <li @click="cancel()">取消</li>
        </ul>
      </div>
    </div>
</template>

<script>
    export default {
        name: "Touxiang",
      data(){
        return{
          bol:false
        }
      },
      methods:{
        dl(){
          this.bol=true;
          $(".center").css("opacity","0.5");
        },
        cancel(){
          this.bol=false;
          $(".center").css("opacity","1");
        }
      }
    }
</script>

<style scoped>
  .wrap{
    margin: 0;
    padding: 0;
    width:72rem;
    height: 128rem;
    background-color:rgb(242,242,242) ;
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
    top: 3rem;
    width: 2.3rem;
    height: 3.8rem;
  }
  .p1{
    position: absolute;
    font-size: 3.6rem;
    color: white;
    left: 30rem;
    top: 3rem;
  }
  .dd img{
    position: absolute;
    width: 3.4rem;
    height: 0.9rem;
    top: 5rem;
    left: 65rem;
  }
  .dayuan{
    position: absolute;
    width: 49.8rem;
    height: 49.8rem;
    border: 1px solid rgb(255,255,255);
    border-radius: 50rem;
    background-color: rgb(255,255,255);
    top: 20rem;
    left: 10rem;
  }
  .tp img{
    position: absolute;
    font-size: 3.6rem;
    top: -0.1rem;
    left: 0.1rem;
    width: 49.8rem;
    height: 49.8rem;
    border-radius: 50rem;
  }
  .bottom{
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 30rem;
    background-color: #fff;
  }
  .ul1{
    list-style-type: none;
    font-size: 2.4rem;
  }
  .ul1 li{
    height: 10rem;
    border-bottom: 1px solid #ccc;
    line-height: 10rem;
  }
</style>
