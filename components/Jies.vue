<template>
<div class="wrap">
  <div class="toubu">
    <p class="p1">结算中心</p>
  </div>
  <div class="add">
   <div class="ls">
     李四
   </div>
    <div class="tel">
      15012340708
    </div>
    <div class="dz">
       河南省新乡市红旗区南干道与新中大道
    </div>
    <div class="jc">
      交叉口B座10楼102室；邮编453000
    </div>
    <div class="yuan">
      <img src="/static/img/ty.png" alt="">
    </div>
    <router-link to="/add2"><div class="dzz">
      修改 <br> 地址
    </div></router-link>
  </div>
  <div class="zf">
   <div class="money">
     本单请支付
   </div>
    <div class="price">
      ¥ 333.80
    </div>
  </div>
  <div class="three">
    <div class="zhifu">
      使用第三方支付平台:
    </div>
  </div>
  <div class="mayun">
    <div class="zhifubao">
      <img src="/static/img/zhifubao.png" alt="">
    </div>
    <div class="zz">
      支付宝支付
    </div>
    <div class="dh">
      <img src="/static/img/wuyanse.png" alt="" @click="nn()" class="img1">
    </div>
  </div>
  <div class="mht" v-show="bol">
  <div class="weixin">
    <img src="/static/img/wixin.png" alt="">
  </div>
    <div class="wx">
      微信支付
    </div>
    <div class="hdh">
      <img src="/static/img/wuyanse.png" alt="" @click="mn()" class="img2">
    </div>
  </div>
  <div class="shou">
  <div class="sq">
    收起
  </div>
    <div class="s">
      <img src="/static/img/shangjian.png" alt="" @click="shou()">
    </div>
  </div>
   <button class="btn" @click="qu()">确认支付</button>
  </div>
</template>

<script>
    export default {
        name: "Jies",
        data(){
          return{
            bol:true,
            n:0,
            arr:[],
            z:0
          }
        },
        methods:{
          nn(){
            this.z++;
            document.getElementsByClassName("img1")[0].src="/static/img/duihao.png"
            document.getElementsByClassName("img2")[0].src="/static/img/wuyanse.png"
          },
          mn(){
            this.z++;
            document.getElementsByClassName("img2")[0].src="/static/img/duihao.png"
            document.getElementsByClassName("img1")[0].src="/static/img/wuyanse.png"
          },
          qu(){
            if(this.z%2!=0,1){
              alert("恭喜您,支付成功!");
            }

          },
          shou(){
            this.n++;
            this.arr.push(this.n);
            if(this.arr.length%2==0){
              this.bol = !this.bol;
              document.getElementsByClassName("shou")[0].style.marginTop="0rem";
            }else{
              this.bol = !this.bol;
              document.getElementsByClassName("shou")[0].style.marginTop="-10rem";
            }
          }

        }
    }
</script>

<style scoped>
.wrap{
  margin: 0;
  padding: 0;
  width: 100%;
  position: relative;
  width: 72rem;
  height: 128rem;
  background-color: rgb(242,242,242);
}
.toubu{
  position: absolute;
  border: 1px solid rgb(229,62,66);
  width: 72rem;
  height: 9.6rem;
  background-color: rgb(229,62,66);
}
.p1{
  position: absolute;
  font-size: 3.6rem;
  color: white;
  left: 30rem;
  top: 3rem;
}
  .add{
    position: absolute;
    width: 72rem;
    height: 22em;
    border: 1px solid rgb(204,204,204);
    top: 9.5rem;
    background-color: white;
  }
  .ls{
    position: absolute;
     font-size:2.8rem;
    left: 2rem;
    top: 1rem;
    color: rgb(77,77,77);
  }
  .tel{
    position: absolute;
    font-size: 2.8rem;
    top: 1rem;
    left: 20rem;
    color:rgb(77,77,77);
  }
  .dz{
    position: absolute;
    font-size: 2.2rem;
    left: 2rem;
    top: 6rem;
    color: rgb(128,128,128);
  }
  .jc{
    position: absolute;
    font-size: 2.2rem;
    top: 9rem;
    left: 2rem;
    color:rgb(128,128,128);
  }
  .yuan img{
    position: absolute;
    width: 8rem;
    height: 8rem;
    left: 60rem;
    top: 3rem;
  }
  .dzz{
    position: absolute;
    font-size: 2.2rem;
    left:61.5rem;
    top: 4rem;
    color: rgb(128,128,128);
  }
  .zf{
    position: absolute;
    border: 1px solid rgb(204,204,204);
    background-color: white;
    width: 72rem;
    height: 10rem;
    top: 27rem;
  }
  .money{
    position: absolute;
    font-size: 2.8rem;
    top: 3rem;
    left: 2rem;
  }
  .price{
    position: absolute;
    font-size: 2.8rem;
    color:rgb(229,62,66);
    left: 58rem;
    top: 3rem;
  }
  .three{
    position: absolute;
    width: 72rem;
    height: 10rem;
    border: 1px solid rgb(204,204,204);
    background-color: white;
    top: 39rem;
  }
  .zhifu{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    top: 3rem;
    left: 2rem;
  }
  .mayun{
    position:absolute ;
    width:72rem;
    height: 10rem;
    border: 1px solid rgb(204,204,204);
    background-color: white;
    top: 49rem;
  }
  .zhifubao img{
    position: absolute;
    left: 2rem;
    width:5rem;
    height: 5rem;
    top: 2.5rem;
  }
  .zz{
    position: absolute ;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    top: 3rem;
    left: 10rem;
  }
  .dh img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    left: 67rem;
    top: 3rem;
  }
  .mht{
    position: absolute;
    border: 1px solid rgb(204,204,204);
    width: 72rem;
    height: 10rem;
    background-color: white;
    top: 59rem;
  }
  .weixin img{
    position: absolute;
    width: 5rem;
    height: 5rem;
  left: 2rem;
    top: 2.5rem;
  }
  .wx{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    top: 3rem;
    left: 10rem;
  }
  .hdh img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    top: 3rem;
    left: 67rem;
  }
  .shou{
    position: absolute;
    width: 72rem;
    height: 6rem;
    background-color: white;
    top: 69.3rem;
  }
  .sq{
    position: absolute;
    font-size: 2.8rem;
    color: #666666;
    left: 30rem;
    top: 1rem;
  }
  .s img{
    position: absolute;
    width: 2.4rem;
    height: 1.4rem;
    left: 37rem;
    top: 2rem;
  }
  .btn{
    position: absolute;
    border: 1px solid rgb(229,62,66);
    border-radius: 3.5rem;
    background-color: rgb(229,62,66);
    color: rgb(255,255,255);
    width: 60rem;
    font-size:2.8rem;
    height: 6.6rem;
    top: 90rem;
    left:6rem;
  }
</style>
