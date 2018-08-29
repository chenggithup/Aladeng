<template>
  <div class="wrap">
    <div class="top">
      <span class="che">购物车</span>
      <span class="fx" @click="it()">编辑</span>
    </div>
     <div class="one">
       <img src="/static/img/gouwu01.png" alt="">
       <button>去分享 ></button>
     </div>
      <ul class="ul1">
        <li class="li1" style="text-align: left">
          <img class="dui duis dui33 dui34" src="/static/img/wuyanse.png" alt="" @click="jio()">
          <img class="feiji" src="/static/img/feiji.png" alt="">
          <span>日本直邮</span>
        </li>
        <li class="li2">
          <img class="dui2 dui02 dui33 du01" src="/static/img/wuyanse.png" alt="" @click="kl()">
          <div class="shangp">
            <img class="tu1" src="/static/img/01.png" alt="">
            <span class="sp1">丝滑</span>
            <span class="sp2">规格 : 蜜粉</span>
            <span class="sp3">¥166.9</span>
          </div>
          <div class="num">
            <span class="jians">-</span><span class="shu">1</span><span class="jias">+</span>
          </div>
        </li>

        <li class="li2">
          <img class="dui2 dui02 dui33 du02" src="/static/img/wuyanse.png" alt="" @click="jk()">
          <div class="shangp">
            <img src="/static/img/01.png" alt="">
            <span class="sp1">丝滑</span>
            <span class="sp2">规格 : 蜜粉</span>
            <span class="sp3">¥166.9</span>

          </div>
          <div class="num">
            <span class="jiansu">-</span>
            <span class="shu">1</span>
            <span class="jiasu">+</span>
          </div>
        </li>

        <li class="li3">
          <span style="float: left;margin-left: -18rem;">商品金额</span><span style="float: right;margin-right: -18rem;" class="qian">{{166.9*this.n | currency('￥',2)}}</span>
        </li>
        <li class="li3">
          <span style="float: left;margin-left: -18rem;">综合税总额</span><span style="float: right;margin-right: -18rem;" class="qian">{{166.9*this.n | currency('￥',2)}}</span>
        </li>
        <li class="li3">
          <span style="float: left;margin-left: -18rem;">应付总额</span><span style="float: right;margin-right: -18rem;" class="qian">{{166.9*this.n | currency('￥',2)}}</span>
        </li>
        <li class="li4" style="margin-left: -5rem;">
          <router-link to="jies"><button @click="jiesuan()" class="jiesuan" style="margin-right: -7rem">结算: <span class="shu01">{{this.n}}</span></button></router-link>
        </li>

      </ul>

    <ul style="margin-top: 2rem;" class="ul1">
      <li class="li1">
        <img class="dui dui33 duis sd" src="/static/img/wuyanse.png" alt="" @click="hh()">
        <img class="feiji" src="/static/img/feiji.png" alt="">
        <span>韩国直邮</span>
      </li>
      <li class="li2">
      <img class="dui2 dui33 sd" src="/static/img/wuyanse.png" alt="">
      <div class="shangp">
        <img src="/static/img/01.png" alt="">
        <span class="sp1">丝滑</span>
        <span class="sp2">规格 : 蜜粉</span>
        <span class="sp3">¥166.9</span>

      </div>
      <div class="num">
        <span class="jiansudu">-</span><span class="shu">1</span><span class="jiasudu">+</span>
      </div>
    </li>


      <li class="li3">
        <span style="float: left;margin-left: -16rem;">商品金额(不含税)</span><span style="float: right;margin-right: -16rem;" class="qian">{{166.06*this.q | currency('￥',2)}}</span>
      </li>
      <li class="li3">
        <span style="float: left;margin-left: -18rem;">综合税总额</span><span style="float: right;margin-right: -18rem;" class="qian">{{0.33*this.q | currency('￥',2)}}</span>
      </li>
      <li class="li3">
        <span style="float: left;margin-left: -18rem;">应付总金额</span><span style="float: right;margin-right: -18rem;" class="qian">{{166.39*this.q | currency('￥',2)}}</span>
      </li>
      <li class="li4" style="margin-left: -5rem;">
        <router-link to="/jies"><button class="jiesuan" style="margin-right: -7rem;margin-top: 1rem">结算: <span class="shu01">{{this.q}}</span></button></router-link>
      </li>

    </ul>

    <ul class="ul1 ul2" style="margin-top: 2rem">
      <li class="li1">
        <img class="dui" src="/static/img/shixiao.png" alt="">
        <span>失效产品</span>
      </li>
      <li class="li2">
        <img class="dui2 dui33" src="/static/img/wuyanse.png" alt="" @click="liang()">
        <div class="shangp">
          <img src="/static/img/01.png" alt="">
          <span class="sp1">丝滑</span>
          <span class="sp2">规格 : 蜜粉</span>
          <span class="sp3">¥166.9 </span>
          <span class="jianshu">X1件</span>
        </div>
      </li>
      <li class="li3">
         <button class="shixiao">清除失效商品</button>
      </li>
    </ul>

      <div class="youlove">
           <div class="love1">
        <div class="d1"></div>
        <span class="mz">猜猜你喜欢的</span>
        <div class="d2"></div>
           </div>
       <div class="love2" style="margin-top: 2rem">
         <div class="kouh">
           <img src="/static/img/kouhong.png" alt=""><br>
            <span>不易脱妆口红</span>
             <p>¥59</p>
         </div>
         <div class="kouh">
           <img src="/static/img/kouhong.png" alt=""><br>
           <span>不易脱妆口红</span>
           <p>¥59</p>
         </div>
         <div class="kouh">
           <img src="/static/img/kouhong.png" alt=""><br>
           <span>不易脱妆口红</span>
           <p>¥59</p>
         </div>
         <div class="kouh">
           <img src="/static/img/kouhong.png" alt=""><br>
           <span>不易脱妆口红</span>
           <p>¥59</p>
         </div>
       </div>

        <div style="margin-top: 4rem" class="love2">
          <div class="kouh">
            <img src="/static/img/kouhong.png" alt=""><br>
            <span>不易脱妆口红</span>
            <p>¥59</p>
          </div>
          <div class="kouh">
            <img src="/static/img/kouhong.png" alt=""><br>
            <span>不易脱妆口红</span>
            <p>¥59</p>
          </div>
          <div class="kouh">
            <img src="/static/img/kouhong.png" alt=""><br>
            <span>不易脱妆口红</span>
            <p>¥59</p>
          </div>
          <div class="kouh">
            <img src="/static/img/kouhong.png" alt=""><br>
            <span>不易脱妆口红</span>
            <p>¥59</p>
          </div>
        </div>


      </div>

  </div>
</template>

<script>
    import Vue from 'vue'
    import axios from 'axios'
    Vue.filter('currency',function(value,arg1,arg2){
      return arg1+value.toFixed(arg2);
    });

    export default {
        name: "Gouwu",
        data(){
          return{
            str:'¥59',
            n:2,
            a:0,
            arr:[],
            q:1,
            t:0,
            arrA:[],
            r:0,
            arrB:[],
            y:0,
            arrC:[],
            arrD:[]
        }
      },
      methods:{
          hh(){
            this.y++;
            this.arrC.push(this.y);
            if(this.arrC.length%2!=0){
              $(".sd").attr("src","/static/img/duihao.png");
            }else{
              $(".sd").attr("src","/static/img/wuyanse.png");
            }
          },
        kl(){
          this.r++;
          this.arrA.push(this.r);
          if(this.arrA.length%2!=0){
            $(".du01").attr("src","/static/img/duihao.png");
          }else{
            $(".du01").attr("src","/static/img/wuyanse.png");
          }
        },
        jk(){
          this.r++;
          this.arrB.push(this.r);
          if(this.arrB.length%2!=0){
            $(".du02").attr("src","/static/img/duihao.png");
          }else{
            $(".du02").attr("src","/static/img/wuyanse.png");
          }
          if(this.r%3==0){
            $(".dui34").attr("src","/static/img/duihao.png");
          }else{
            $(".dui34").attr("src","/static/img/wuyanse.png");
          }
        },
        liang(){
          this.a++;
          this.arr.push(this.a);
          if(this.arr.length%2!=0){
            $(this).attr("src","/static/img/duihao.png");
            $(".shixiao").click(function () {
              $(".shixiao").parent().parent().remove();
            })
          }
        },
        it(){
          this.a++;
          this.arr.push(this.a);
          if(this.arr.length%2!=0){
            $(".dui33").css("display","block");
          }else{
            $(".dui33").css("display","none");
          }

        },
        jio(){
          this.t++;
          this.arrA.push(this.t);
          if(this.arrA.length%2!=0){
            $(".dui34").attr("src","/static/img/duihao.png");
            $(".dui02").attr("src","/static/img/duihao.png");
          }else{
            $(".dui34").attr("src","/static/img/wuyanse.png");
            $(".dui02").attr("src","/static/img/wuyanse.png");
          }
        },
        jiesuan(){
          var name = $('.sp1').html();
          var ms = $('.sp2').html();
          var jiage = $('.sp3').html();
          var num = $('.shu01').html();
          var price = $('.qian').html();
          var src = $('.tu1').attr('src');
          var params = new URLSearchParams();
          params.append('name',name);
          params.append('miaoshu',ms);
          params.append('jiage',jiage);
          params.append('num',num);
          params.append('price',price);
          params.append('src',src);
          axios.post('/api/phph0302/shop.php',params).then(function(res){
            console.log(res.data);
          }.bind(this));
        }
      },

     mounted:function(){
       var srcs = ['/static/img/duihao.png','/static/img/wuyanse.png'];
       var bols=true;
       var bols2 = false;
       var _this = this;
       $('.duis').click(function () {
         _this.bols2 = !_this.bols2;
         if (_this.bols2==true){
           $(this).attr({
             src:srcs[0]
           });
           $('.dui02').attr({
             src:srcs[0]
           });
         }else if(_this.bols2==false){
           $(this).attr({
             src:srcs[1]
           });
           $('.dui02').attr({
             src:srcs[1]
           });
         }
       });

       $('.dui2').click(function(){
         _this.bols = !_this.bols;
         if (_this.bols==true){
           $(this).attr({
             src:srcs[0]
           });
           console.log('bols的值='+bols);
         }else if(_this.bols==false){
           $(this).attr({
             src:srcs[1]
           });
           console.log('bols的值='+bols);
         }
       });


       //购物车数量
       var a=1;
       var b=1;
       var c=1;
       $('.jians').click(function(){
         if(a<=1){
           alert("不能再点击了")
         }else{
           a--;
           _this.n--;
         }
         $(this).next().html(a);
       });

       $('.jiansu').click(function(){
         if(b<=1){
           alert("不能再点击了")
         }else{
           b--;
           _this.n--;
         }
         $(this).next().html(b);
       });
       $('.jiansudu').click(function(){
         if(c<=1){
           alert("不能再点击了")
         }else{
           c--;
           _this.q--;
         }
         $(this).next().html(c);
       });

       $('.jiasudu').click(function(){
         c++;
         _this.q++;
         if(c>9){
           _this.c=9;
         }
         $(this).prev().html(c);
       });

       $('.jias').click(function(){
         a++;
         _this.n++;
         if(a>9){
           _this.a=9;
         }
         $(this).prev().html(a);
       });

       $('.jiasu').click(function(){

         b++;
         _this.n++;
         if(b>9){
           _this.b=9;
         }

         $(this).prev().html(b);
       });

     }

    }
</script>

<style scoped>
  *{margin: 0;padding: 0;}
  .wrap{width: 100%;background: #f2f2f2;
    height: 100%;
    text-align: left;
  }
  .top{background-color: red;
    height: 9.6rem;
    width: 100%;
    position: relative;
  }
  .fx{
    position: absolute;
    font-size: 3rem;
    right: 2rem;
    top: 3.3rem;
    color: white;
  }
  .che{
    position: absolute;
    font-size: 3.6rem;
    left: 30rem;
    top: 3rem;
    color: white;
  }
  .one img{
    width: 100%;
    height: 100%
  }
  .ul1{
    margin-top: -14rem;
    list-style-type: none;
    background-color: white;
  }
  .feiji{
    width: 3.3rem;
    height: 3.3rem;
  }
.li1{
  width: 100%;
  height: 8rem;
  border-bottom: 1px #cccccc solid;
  line-height: 8rem;
  position: relative;
}
.li1 span{
  font-size: 2.8rem;
  color: #4d4d4d;
  padding: 1rem;
  position: absolute;
  left: 10rem;
  top: 0rem;
}
.li1 img:nth-child(1){
  position: absolute;
  left: 0.5rem;
  top: 1rem;
}
  .dui,.dui2{
    width: 3rem;
    height: 3rem;
    margin-top: 2rem;
    margin-left: 2rem;
  }
  .dui2{
    position: absolute;
    top: 8rem;
  }
  .feiji{
    width: 3.4rem;
    height: 3.3rem;
    padding-left: 6rem;
    margin-top: 3rem;

  }
  .li2{
    position: relative;
    width: 100%;
    height: 20rem;
    border-bottom:1px #cccccc solid;
  }
.shangp{
  position: absolute;
  left: 10rem;
  top:5rem;
  width: 32.9rem;
  height: 14.1rem;
}
.shangp img{
  width: 8.6rem;
  height: 10rem;
}
  .sp1{
    position: absolute;
    top: 0rem;
    left: 17rem;
    font-size: 2.8rem;
    color: #4d4d4d;
  }
.sp2{
  position: absolute;
  top: 5rem;
  left: 17rem;
  font-size: 2.4rem;
  color: #666666;
}
  .sp3{
    position: absolute;
    left: 17rem;
    top: 10rem;
    font-size: 2.4rem;
    color: red;
  }
  .num{
    width: 16rem;
    height: 4.8rem;
    border-radius: 2rem;
    border: 1px #cccccc solid;
    text-align: center;
    position: absolute;
    right: 2rem;
    line-height: 4.8rem;
    bottom: 1.6rem;
  }
  .num span{
    font-size: 3.6rem;
    display: inline-block;
  }
  .jias,.jians{
    width: 4rem;
    height: 4rem;
    border-radius: 50%;
    border: 1px #cccccc solid;
    text-align: center;
    line-height: 4rem;
    margin-top: 0.5rem;
  }
  .jiasu,.jiansu{
    width: 4rem;
    height: 4rem;
    border-radius: 50%;
    border: 1px #cccccc solid;
    text-align: center;
    line-height: 4rem;
    margin-top: 0.5rem;
  }
  .jiasudu,.jiansudu{
    width: 4rem;
    height: 4rem;
    border-radius: 50%;
    border: 1px #cccccc solid;
    text-align: center;
    line-height: 4rem;
    margin-top: 0.5rem;
  }
.shu{
  position: absolute;
  left: 7rem;
  }
  .jias,.jiasu,.jiasudu{
    margin-left: 7rem;
  }

  .li3{
    display: flex;
    justify-content: space-around;
    border-bottom: 1px solid #cccccc;
    width: 100%;
    height: 8rem;
  }
  .li3 span{
    display: inline-block;
    font-size: 2.8rem;
    margin-top: 2rem;
  }
  .qian{
    color: red;
  }
  .li4{
    width: 100%;
    height: 8rem;
    position: relative;
    border-bottom: 1px #cccccc solid;
  }
  .jiesuan{
    width: 14rem;
    height: 4.8rem;
    background-color: red;
    border-radius: 2rem;
    font-size: 2.8rem;
    color: white;
    position: absolute;
    right: 4rem;
    top:1.5rem;
  }

  .jianshu{
    color: #808080;
    font-size: 2.8rem;
   margin-left: 25rem;
  }
  .shixiao{
    width: 30rem;
    height: 4.6rem;
    border-radius: 2rem;
    border: 1px #cccccc solid;
    font-size: 2.4rem;
    color: #4d4d4d;
    background-color: white;
    margin-top: 2rem;
  }
  .youlove{
    text-align: center;
    position: relative;
    margin-top: 3rem;
    background-color: white;
  }

  .mz{
    display: inline-block;
    font-size: 3rem;
    color: #4d4d4d;
    margin-top: 4.3rem;
  }
  .d1,.d2{
    width: 70px;
    height: 2px;background: #cccccc;
  }
  .love1{position: relative;}
  .d1{position: absolute;left: 22rem;top:6.5rem}
  .d2{position: absolute;right: 22rem;top:6.5rem}


  .love2{
    width: 100%;
    display: flex;
    justify-content: space-around;
  }
  .kouh{width: 18.1rem;
    height: 20rem;
    border-right: 1px #cccccc solid;
  }
.kouh img{
  width: 9rem;
  height: 14rem;

}
.kouh span{font-size: 2.4rem;}
  .kouh p {font-size: 2.4rem;color: red;}
  .one{
    position: relative;
  }
  .one button{
    width: 12rem;
    height: 4rem;
    background-color: #ffffff;
    color: #808080;
    font-size: 2.4rem;
    position: absolute;
    right: 14rem;
    top: 10rem;
  }
  .dui33{
    display: none;
  }
</style>
