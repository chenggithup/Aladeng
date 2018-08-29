<template>
    <div class="wrap">
      <div class="toubu"></div>
      <div class="zuo">
        <router-link to="/shiming"><img src="/static/img/zuo.png" alt=""></router-link>
      </div>
      <p class="p1">身份实名认证</p>
      <div class="xx">
        身份信息
      </div>
      <div class="sh">
        请确保身份证信息真实有效，否则无法通过审核
      </div>
      <input class="nam" type="text" placeholder="您的姓名 (请填写身份证上的真实姓名)" value="">
        <input class="jiam" type="text" placeholder="您的身份证号（将加密处理）">
      <div class="pict">
        身份证照片
      </div>
      <div class="sc">
        上传身份证正反面照片让通关更便捷
      </div>
      <div class="shen">
        <div class="ren">
       <div class="rx">
         <img src="/static/img/zhengmian.png" alt="">
       </div>
          <div class="ssc">
            请上传
          </div>

        </div>
        <div class="gh">
          <div class="guohui">
            <img src="/static/img/fanmian.png" alt="">
          </div>
          <div class="ssw">
            请上传
          </div>
        </div>
         <div class="shc">
           *上传前请先查看样张
         </div>
        <div class="wh">
          <img src="/static/img/hongwenhao.png" alt="">
        </div>
        <div class="help">
          查看更多帮助内容
        </div>
      </div>
       <div class="cxc">
        <div class="tp"></div>
       </div>
         <div class="ghh">
           <div class="cc"></div>
         </div>
      <div class="why">
        <div class="what">
          为什么需要实名认证？
        </div>
      </div>
      <div class="ss">
      <div class="rj">
        根据海关规定，购买跨境商品需要办理清关手续，需要您上传身份证信息用于商品
      </div>
        <div class="jc">
          入境申报真实的姓名和身份信息才能确保您的包裹顺利通过海关检查
        </div>
        <div class="shm">
          声明：阿拉灯负责提交信息，并对您的身份信息保密，绝不传播或用于其他地方
        </div>
        <div class="fangx">
          请放心填写。
        </div>
      </div>
      <div class="slic">
        <button class="btn" @click="ti()">提交</button>
      </div>
    </div>

</template>
<script>
    export default {
        name: "Shiming1",
        methods:{
          ti(){
            this.$router.push("/shiming2");
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
    left: 25rem;
    top: 3rem;
  }
  .xx{
    position: absolute;
    font-size: 2.4rem;
    color: #666666;
    top: 11rem;
    left:2rem ;
  }
  .sh{
    position: absolute;
    font-size:1.8rem;
    color: rgb(229,62,66);
    top: 11.5rem;
    left: 15rem;
  }
  .nam{
   position: absolute;
    width: 72rem;
    height: 8rem;
    top: 15rem;
    color: rgb(204,204,204);
    font-size:2.8rem;
    left: 0.1rem;
  }
  .jiam{
    position: absolute;
    width: 72rem;
    height: 8rem;
    top: 23.2rem;
    color: rgb(204,204,204);
    font-size:2.8rem;
    left: 0.1rem;
  }
  .pict{
    position: absolute;
    font-size: 2.4rem;
    color: #666666;
    top: 32rem;
    left: 2rem;
  }
  .sc{
    position: absolute;
    font-size: 1.8rem;
    color:rgb(229,62,66);
    top: 32.6rem;
    left: 15rem;
  }
  .shen{
    position: absolute;
    width: 72rem;
    height: 62rem;
    background-color:rgb(255,255,255) ;
    top: 36rem;
  }
  .ren{
    position: absolute;
    width: 28rem;
    height: 20rem;
    border: 1px solid rgb(204,204,204) ;
    top: 4rem;
    left: 5rem;
  }
  .rx img{
    position: absolute;
    width: 10.6rem;
    height: 7.6rem;
    top:4rem;
    left: 9rem;
  }
  .ssc{
    position: absolute;
    font-size:2.4rem;
    color: #666666;
    top: 13rem;
    left: 10rem;
  }
  .gh{
    position: absolute;
    width: 28rem;
    height: 20rem;
    position: absolute;
    width: 28rem;
    height: 20rem;
    border: 1px solid rgb(204,204,204);
    left: 39rem;
    top: 4rem;
  }
  .guohui img{
    position: absolute;
    width: 10.6rem;
    height: 7.6rem;
    top:4rem;
    left: 9rem;
  }
  .ssw {
    position: absolute;
    font-size: 2.4rem;
    color: #666666;
    top: 13rem;
    left: 10rem;
  }
  .shc{
    position: absolute;
    font-size: 1.8rem;
    color: rgb(229,62,66);
    top: 27rem;
    left: 10rem;
  }
  .wh img{
    position: absolute;
    width: 2.4rem;
    height: 2.4rem;
    top: 27rem;
    left: 44rem;
  }
  .help{
    position: absolute;
    font-size: 1.8rem;
    color: rgb(229,62,66);
    top: 27rem;
    left: 47rem;
  }
  .cxc{
    position: absolute;
    width: 22rem;
    height:28rem;
    border: 1px solid rgb(204,204,204);
    top: 68rem;
    left: 8rem;
  }
  .tp{
    position: absolute;
    width: 22rem;
    height: 16rem;
    border: 1px solid rgb(204,204,204);
    background-color: #f2f2f2;
  }
  .ghh{
    position: absolute;
    width: 22rem;
    height:28rem;
    border: 1px solid rgb(204,204,204);
    top: 68rem;
    left: 40rem;
  }
  .cc{
    position: absolute;
    width: 22rem;
    height: 16rem;
    border: 1px solid rgb(204,204,204);
    background-color: #f2f2f2;
  }
  .why{
    position: absolute;
    width: 72rem;
    height: 4rem;
    background-color: rgb(249,211,212);
    top: 99.5rem;
  }
  .what{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(229,62,66);
    left: 25rem;
  }
  .ss{
    position: absolute;
    width: 72rem;
    height: 16rem;
    background-color:rgb(255,255,255);
    top: 103.7rem;
  }
  .rj{
    position: absolute;
    font-size: 1.8rem;
    left: 2rem;
    top: 0.5rem;
  }
  .jc{
    position: absolute;
    font-size: 1.8rem;
    top: 4rem;
    left: 2rem;
  }
  .shm{
    position: absolute;
    font-size: 1.8rem;
    top: 9rem;
    left: 2rem;
  }
  .fangx{
    position: absolute;
    font-size: 1.8rem;
    top: 12rem;
    left: 2rem;
  }
  .slic{
    position: absolute;
    width: 72rem;
    height: 9rem;
    background-color:rgb(255,255,255);
    top: 122rem;
  }
  .slic button{
    position: absolute;
    width: 20.5rem;
    height: 3.8rem;
    background-color:rgb(229,62,66) ;
    border-radius: 25rem;
    top: 2.5rem;
    left: 25rem;
  }
  .btn{
    font-size:1.8rem;
    color:rgb(255,255,255) ;
  }
</style>
