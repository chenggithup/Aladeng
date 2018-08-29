<template>
  <div class="wrap">
    <div class="toubu"></div>
    <div class="zuo">
      <router-link to="shz"><img src="/static/img/zuo.png" alt=""></router-link>
    </div>
    <p class="p1">兑换记录</p>
    <div class="p2">
      <p><span @click="edit()">清空</span>|<span @click="edit()">编辑</span></p>
    </div>
    <div class="date">
      <div class="riqi">
        2017-07-03
      </div>
    </div>
    <div class="duihuan">
    <div class="xian"></div>
      <div class="duihao">
        <img src="/static/img/wuyanse.png" alt="" @click="nu()">
      </div>
      <div class="tp">
        <img src="/static/img/chuncai.png" alt="">
      </div>
      <div class="hc">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="japan">
        <img src="/static/img/riben.png" alt="">
      </div>
      <div class="fly">
        <img src="/static/img/feiji.png" alt="">
      </div>
      <div class="hai">
        海外直邮
      </div>
      <div class="price">
        500
      </div>
      <div class="gold">
        <img src="/static/img/niaohu.png" alt="">
      </div>
      <div class="jiaqian">
        ¥ 166.06
      </div>
      <div class="del"></div>
      <div class="yidu">
       <p>已兑换</p>
      </div>
      <div class="date1">
        2017-07-09
      </div>
    </div>
    <div class="duihuan1">
      <div class="xian1"></div>
      <div class="duihao1">
        <img src="/static/img/wuyanse.png" alt="" @click="nu1()">
      </div>
      <div class="tp1">
        <img src="/static/img/chuncai.png" alt="">
      </div>
      <div class="hc1">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="japan1">
        <img src="/static/img/riben.png" alt="">
      </div>
      <div class="fly1">
        <img src="/static/img/feiji.png" alt="">
      </div>
      <div class="hai1">
        海外直邮
      </div>
      <div class="price1">
        500
      </div>
      <div class="gold1">
        <img src="/static/img/niaohu.png" alt="">
      </div>
      <div class="jiaqian1">
        ¥ 166.06
      </div>
      <div class="del1"></div>
      <div class="yidu1">
        <p>已兑换</p>
      </div>
  </div>
    <div class="duihuan2">
      <div class="xian2"></div>
      <div class="duihao2">
        <img src="/static/img/wuyanse.png" alt="" @click="nu2()">
      </div>
      <div class="tp2">
        <img src="/static/img/chuncai.png" alt="">
      </div>
      <div class="hc2">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="japan2">
        <img src="/static/img/riben.png" alt="">
      </div>
      <div class="fly2">
        <img src="/static/img/feiji.png" alt="">
      </div>
      <div class="hai2">
        海外直邮
      </div>
      <div class="price2">
        500
      </div>
      <div class="gold2">
        <img src="/static/img/niaohu.png" alt="">
      </div>
      <div class="jiaqian2">
        ¥ 166.06
      </div>
      <div class="del2"></div>
      <div class="yidu2">
        <p>已兑换</p>
      </div>
    </div>
    <div class="duihuan3">
      <div class="xian3"></div>
      <div class="duihao3">
        <img src="/static/img/wuyanse.png" alt="" @click="nu3()">
      </div>
      <div class="tp3">
        <img src="/static/img/chuncai.png" alt="">
      </div>
      <div class="hc3">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="japan3">
        <img src="/static/img/riben.png" alt="">
      </div>
      <div class="fly3">
        <img src="/static/img/feiji.png" alt="">
      </div>
      <div class="hai3">
        海外直邮
      </div>
      <div class="price3">
        500
      </div>
      <div class="gold3">
        <img src="/static/img/niaohu.png" alt="">
      </div>
      <div class="jiaqian3">
        ¥ 166.06
      </div>
      <div class="del3"></div>
      <div class="yidu3">
        <p>已兑换</p>
      </div>
    </div>
    <div class="bottom" v-show="bol">
      <img @click="ji()" src="/static/img/wuyanse.png" alt="">
      <span>全选</span>
      <button class="shan">删除</button>
    </div>
    </div>
</template>

<script>
    export default {
        name: "Jilu",
        data(){
          return{
            bol:false,
            n:0,
            count:0,
            arr:[]
          }
        },
        methods:{
          edit(){
            this.bol=!this.bol;
            $(".duihao img").css("display","block");
            $(".duihao1 img").css("display","block");
            $(".duihao2 img").css("display","block");
            $(".duihao3 img").css("display","block");
          },
          nu(){
            var _this=this;
            _this.n++;
            _this.arr.push(_this.n);
            if(_this.arr.length%2!=0){
                $(".duihao").find("img").attr("src","/static/img/duihao.png");
              _this.count++;
              $(".shan").click(function () {
                $('.duihao').parent().remove();
              })
            }else{
              $(".duihao").find("img").attr("src","/static/img/wuyanse.png");
              $(".bottom img").attr("src","/static/img/wuyanse.png");
            }
          },
          nu1(){
            var _this=this;
            _this.n++;
            _this.arr.push(_this.n);
            if(_this.arr.length%2!=0){
              $(".duihao1").find("img").attr("src","/static/img/duihao.png");
              _this.count++;
              $(".shan").click(function () {
                $('.duihao1').parent().remove();
              })
            }else{
              $(".duihao1").find("img").attr("src","/static/img/wuyanse.png");
              $(".bottom img").attr("src","/static/img/wuyanse.png");
            }
          },
          nu2(){
            var _this=this;
            _this.n++;
            _this.arr.push(_this.n);
            if(_this.arr.length%2!=0){
              $(".duihao2").find("img").attr("src","/static/img/duihao.png");
              _this.count++;
              $(".shan").click(function () {
                $('.duihao2').parent().remove();
              })
            }else{
              $(".duihao2").find("img").attr("src","/static/img/wuyanse.png");
              $(".bottom img").attr("src","/static/img/wuyanse.png");
            }
          },
          nu3(){
            var _this=this;
            _this.n++;
            _this.arr.push(_this.n);
            if(_this.arr.length%2!=0){
              $(".duihao3").find("img").attr("src","/static/img/duihao.png");
              _this.count++;
              console.log(_this.count);
              if(_this.count%4%2==0,1,2,3,4,5,6,7,8,9){
                $(".bottom img").attr("src","/static/img/duihao.png");
              }
              $(".shan").click(function () {
                $('.duihao3').parent().remove();
              })
            }else{
              $(".duihao3").find("img").attr("src","/static/img/wuyanse.png");
              $(".bottom img").attr("src","/static/img/wuyanse.png");
            }
          },
          ji(){
            $(".bottom img").attr("src","/static/img/duihao.png");
            $(".duihao img").attr("src","/static/img/duihao.png");
            $(".duihao1 img").attr("src","/static/img/duihao.png");
            $(".duihao2 img").attr("src","/static/img/duihao.png");
            $(".duihao3 img").attr("src","/static/img/duihao.png");
            $(".shan").click(function () {
              $('.duihao').parent().remove();
              $('.duihao2').parent().remove();
              $('.duihao3').parent().remove();
              $('.duihao1').parent().remove();
              $(".bottom").remove();
              $(".date").remove();
            })
          }
        }
    }
</script>

<style scoped>
  .bottom{
    position: fixed;
    left: 0;
    bottom: 0;
    height: 10rem;
    background-color: #fff;
    width: 100%;
    text-align: left;
  }
  .bottom img{
    width: 3rem;
    height: 3rem;
    margin-left: 2rem;
    margin-top: 4rem;
  }
  .bottom span{
    font-size: 3rem;
    margin-left: 2rem;
    margin-top: 4rem;
  }
  .bottom button{
    width: 12.6rem;
    height: 4rem;
    border-radius: 2rem;
    background-color: #f00;
    font-size: 3rem;
    color: #fff;
    margin-left: 40rem;
  }

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
  .p2{
    position: absolute;
    font-size: 3rem;
    color: rgb(255,255,255);
    top: 3rem;
    left: 57rem;
  }
  .date{
    position: absolute;
    border: 1px solid rgb(204,204,204);
    background-color:rgb(255,255,255);
    width: 72rem;
    height: 6rem;
    top: 9.5rem;
  }
  .riqi{
    position: absolute;
    font-size: 2.8rem;
    color: #666666;
    left: 2rem;
    top: 1.5rem;
  }
  .duihuan{
    position: absolute;
    /*border: 1px solid rgb(204,204,204);*/
    background-color:rgb(255,255,255);
    width: 72rem;
    height: 26rem;
    top: 15.7rem;
  }
  .xian{
    position: absolute;
    width: 52rem;
    height: 0.1rem;
    border: 0.5px solid rgb(204,204,204);
    top: 20rem;
    left: 20rem;
  }
  .tp img{
    position: absolute;
    width: 6.9rem;
    height: 15.3rem;
    top: 2rem;
    left: 7rem;
  }
  .hc{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    top: 2rem;
    left: 20rem;
  }
  .japan img{
    position: absolute;
    width: 3rem;
    height: 2rem;
    left: 20rem;
    top: 10rem;
  }
  .fly img{
    position: absolute;
    width: 3.4rem;
    height: 3.3rem;
    top: 9rem;
    left: 25rem;
  }
  .hai{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(102,102,102);
    top: 9rem;
    left: 30rem;
  }
  .price{
    position: absolute;
    font-size: 3rem;
    color:rgb(229,62,66);
    top: 15rem;
    left: 20rem;
  }
  .gold img{
    position: absolute;
    width: 2.4rem;
    height: 1.6rem;
    top: 16rem;
    left: 25.5rem;
  }
  .duihao img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    left: 2rem;
    top: 8rem;
    display: none;
  }
  .jiaqian{
    position: absolute;
    font-size: 2.4rem;
    top: 15.5rem;
    left: 30rem;
    color: rgb(128,128,128);
  }
  .del{
    position: absolute;
    border: 1px solid grey;
    width: 10rem;
    height: 0.2rem;
    top: 16.8rem;
    left: 29.5rem;
  }
  .yidu{
    position: absolute;
    width: 12rem;
    height: 4rem;
    background-color: rgb(229,62,66);
    border-radius: 25rem;
    top: 14.7rem;
    left: 58rem;
  }
  .yidu p{
    position: absolute;
    font-size: 2.8rem;
    color: white;
    left: 2rem;
  }
  .date1{
    position: absolute;
    font-size: 2.8rem;
    color: #666666;
    top: 21rem;
    left: 2rem;
  }
  .duihuan1{
    position: absolute;
    /*border: 1px solid rgb(204,204,204);*/
    background-color:rgb(255,255,255);
    width: 72rem;
    height: 20rem;
    top: 41.9rem;
  }
  .xian1{
    position: absolute;
    width: 52rem;
    height: 0.1rem;
    border: 0.5px solid rgb(204,204,204);
    top: 20rem;
    left: 20rem;
  }
  .tp1 img{
    position: absolute;
    width: 6.9rem;
    height: 15.3rem;
    top: 2rem;
    left: 7rem;
  }
  .hc1{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    top: 2rem;
    left: 20rem;
  }
  .japan1 img{
    position: absolute;
    width: 3rem;
    height: 2rem;
    left: 20rem;
    top: 10rem;
  }
  .fly1 img{
    position: absolute;
    width: 3.4rem;
    height: 3.3rem;
    top: 9rem;
    left: 25rem;
  }
  .hai1{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(102,102,102);
    top: 9rem;
    left: 30rem;
  }
  .price1{
    position: absolute;
    font-size: 3rem;
    color:rgb(229,62,66);
    top: 15rem;
    left: 20rem;
  }
  .gold1 img{
    position: absolute;
    width: 2.4rem;
    height: 1.6rem;
    top: 16rem;
    left: 25.5rem;
  }
  .duihao1 img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    left: 2rem;
    top: 8rem;
    display: none;
  }
  .jiaqian1{
    position: absolute;
    font-size: 2.4rem;
    top: 15.5rem;
    left: 30rem;
    color: rgb(128,128,128);
  }
  .del1{
    position: absolute;
    border: 0.5px solid grey;
    width: 10rem;
    height: 0.2rem;
    top: 16.8rem;
    left: 29.5rem;
  }
  .yidu1{
    position: absolute;
    width: 12rem;
    height: 4rem;
    background-color: rgb(229,62,66);
    border-radius: 25rem;
    top: 14.7rem;
    left: 58rem;
  }
  .yidu1 p {
    position: absolute;
    font-size: 2.8rem;
    color: white;
    left: 2rem;
  }
  .duihuan2{
     position: absolute;
     /*border: 1px solid rgb(204,204,204);*/
     background-color:rgb(255,255,255);
     width: 72rem;
     height: 20rem;
     top: 62rem;
   }
  .xian2{
    position: absolute;
    width: 52rem;
    height: 0.1rem;
    border: 0.5px solid rgb(204,204,204);
    top: 20rem;
    left: 20rem;
  }
  .tp2 img{
    position: absolute;
    width: 6.9rem;
    height: 15.3rem;
    top: 2rem;
    left: 7rem;
  }
  .hc2{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    top: 2rem;
    left: 20rem;
  }
  .japan2 img{
    position: absolute;
    width: 3rem;
    height: 2rem;
    left: 20rem;
    top: 10rem;
  }
  .fly2 img{
    position: absolute;
    width: 3.4rem;
    height: 3.3rem;
    top: 9rem;
    left: 25rem;
  }
  .hai2{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(102,102,102);
    top: 9rem;
    left: 30rem;
  }
  .price2{
    position: absolute;
    font-size: 3rem;
    color:rgb(229,62,66);
    top: 15rem;
    left: 20rem;
  }
  .gold2 img{
    position: absolute;
    width: 2.4rem;
    height: 1.6rem;
    top: 16rem;
    left: 25.5rem;
  }
  .duihao2 img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    left: 2rem;
    top: 8rem;
    display: none;
  }
  .jiaqian2{
    position: absolute;
    font-size: 2.4rem;
    top: 15.5rem;
    left: 30rem;
    color: rgb(128,128,128);
  }
  .del2{
    position: absolute;
    border: 1px solid grey;
    width: 10rem;
    height: 0.2rem;
    top: 16.8rem;
    left: 29.5rem;
  }
  .yidu2{
    position: absolute;
    width: 12rem;
    height: 4rem;
    background-color: rgb(229,62,66);
    border-radius: 25rem;
    top: 14.7rem;
    left: 58rem;
  }
  .yidu2 p {
    position: absolute;
    font-size: 2.8rem;
    color: white;
    left: 2rem;
  }
  .duihuan3{
    position: absolute;
    /*border: 1px solid rgb(204,204,204);*/
    background-color:rgb(255,255,255);
    width: 72rem;
    height: 20rem;
    top: 82rem;
  }
  .xian3{
    position: absolute;
    width: 52rem;
    height: 0.1rem;
    border: 0.5px solid rgb(204,204,204);
    top: 20rem;
    left: 20rem;
  }
  .tp3 img{
    position: absolute;
    width: 6.9rem;
    height: 15.3rem;
    top: 2rem;
    left: 7rem;
  }
  .hc3{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    top: 2rem;
    left: 20rem;
  }
  .japan3 img{
    position: absolute;
    width: 3rem;
    height: 2rem;
    left: 20rem;
    top: 10rem;
  }
  .fly3 img{
    position: absolute;
    width: 3.4rem;
    height: 3.3rem;
    top: 9rem;
    left: 25rem;
  }
  .hai3{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(102,102,102);
    top: 9rem;
    left: 30rem;
  }
  .price3{
    position: absolute;
    font-size: 3rem;
    color:rgb(229,62,66);
    top: 15rem;
    left: 20rem;
  }
  .gold3 img{
    position: absolute;
    width: 2.4rem;
    height: 1.6rem;
    top: 16rem;
    left: 25.5rem;
  }
  .duihao3 img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    left: 2rem;
    top: 8rem;
    display: none;
  }
  .jiaqian3{
    position: absolute;
    font-size: 2.4rem;
    top: 15.5rem;
    left: 30rem;
    color: rgb(128,128,128);
  }
  .del3{
    position: absolute;
    border: 1px solid grey;
    width: 10rem;
    height: 0.2rem;
    top: 16.8rem;
    left: 29.5rem;
  }
  .yidu3{
    position: absolute;
    width: 12rem;
    height: 4rem;
    background-color: rgb(229,62,66);
    border-radius: 25rem;
    top: 14.7rem;
    left: 58rem;
  }
  .yidu3 p {
    position: absolute;
    font-size: 2.8rem;
    color: white;
    left: 2rem;
  }
</style>
