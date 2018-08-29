<template>
   <div v-if="bol" class="wrap">
     <div class="top">
       <img @click="xiulian()" src="/static/img/fanhui.png" alt="">
       <span>商品详情</span>
        <div class="right">
       <img @click="fenx()" style="width: 3.8rem;height: 3.6rem;" class="gouwu" src="/static/img/gouwu.png" alt="">
        <img class="fx" src="/static/img/fenxiang.png" alt="">
          <img class="zhuye" src="/static/img/shouye.png" alt="" @click="xiulian()">
        </div>
     </div>
     <!--轮播组件-->
     <Lunbo02></Lunbo02>

     <div class="one">
       <div class="one1">
       <img src="/static/img/miziqi.png" alt="">
         <span class="sp1">英国直邮</span> <span class="sp2">不易脱妆口红</span>
         <p class="p1">¥169</p>
         <span class="sp3">关税 : ¥10</span>  <span class="sp4">详情 ></span>
         <p class="p2">邮费 : ¥50</p>
       </div>
       <div class="one2">
         <span class="jifen">积分购</span>
         <span class="aa">500000积分可抵500元, 限购一件</span>
       </div>
       <div class="one3">
         <img class="img1" src="/static/img/buzhichi.png" alt="">
         <span style="color: red;">不支持7天无忧退换</span>
         <img class="img1" src="/static/img/zhiyou.png" alt="">
         <span>海外直邮</span>
         <img class="img1" src="/static/img/zheng.png" alt="">
         <span>正品保障</span>
         <img class="you" src="/static/img/you.png" alt="">
       </div>
       <div class="one4">
         <img src="/static/img/miziqi.png" alt="">
         <span>直邮,下单时需要提供真实姓名和身份证号以及收获地址,</span>
         <span>请去添加并填写这些信息</span>
         <router-link to="/gouwu"><button class="tj">去添加</button></router-link>
       </div>
     </div>

     <div class="two">
       <span class="logo">阿拉丁LOGO</span>
       <span style=" font-size: 3rem;">阿拉灯网站首页LOGO部分的主要内容</span>
       <p>阿拉灯精选</p>
     </div>
     <div class="three">
       <h2>商品信息</h2>
       <p>【品  牌】 ANFNA</p>
       <p>【规  格】 128/支</p>
       <p>【产  地】 英国</p>
       <p>【储存方法】 常温</p>
       <p>【保质期】 2年</p>
       <p>【生产日期】 见实物外包装</p>
       <p>【快递信息】 快递100</p>
       <p>【服务信息】 有品牌商c从英国发货</p>
       <p>【温馨提示】 本产品为易碎品,请轻拿轻放</p>
     </div>

     <div class="four">
       <div class="xian1"></div> <span class="pinpai">品牌承诺</span> <div class="xian2"></div>
       <div class="four1">
         <img src="/static/img/zheng02.png" alt=""><br>
         <span>正品保证</span>
       </div>
       <div class="four1">
         <img src="/static/img/feiji.png "alt=""><br>
         <span>海外直邮</span>
       </div>
       <div class="four1">
         <img src="/static/img/butie02.png" alt=""><br>
         <span>超时发货补贴</span>
       </div>
       <div class="four2">
         <img src="/static/img/picc.png" alt=""><br>
         <span>PICC承诺</span>
       </div>

     </div>

     <div class="five">
       <div class="five1">
         <img src="/static/img/xiaotieshi.png" alt="">
         <span>平台卖家提供发票和相应的售后服务。请您放心购买！
注：因厂家会在没有任何提前通知的情况下更改产品包装、产地或者一些附件，本司不能确保客户收到的货物与商城图片、产地、附件说明完全一致。只能确保为原厂正货！并且保证与当时市场上同样主流新品一致。若本商城没有及时更新，请大家谅解！二级开发框架儿科关联方借款洛克菲勒但考虑到法律热加工GIF入口为顾客反馈给开了放款快乐发快递开了房背带裤三个为几个人看过来人看过来看房人来看过来放开了个开放让刚进入疯狂过付款了;公开发了;乐翻了两浪费了</span>
       </div>
     </div>

    <div class="six">
      <div class="tuijian"><span class="tuijian02">热卖推荐</span></div>
      <div class="six02">
        <img :src="arr[15].src" alt=""><br>
        <p>{{arr[15].names}}</p>
        <span>{{arr[15].jiage}}</span>
      </div>
      <div class="six03">
        <img :src="arr[16].src" alt=""><br>
        <p>{{arr[16].names}}</p>
        <span>{{arr[16].jiage}}</span>
      </div>
    </div>

     <div class="seven">
       <span>继续拖动查看图片详情</span>
     </div>

     <div class="eight">
       <span @click="xian()">在线客服</span> <span @click="gwc()">加入购物车</span>
     </div>

   </div>
</template>

<script>
  import axios from 'axios'
  import Lunbo02 from '@/components/Lunbo02'
    export default {
        name: "koured",
        data(){
          return{
            bol:false,
            arr:[]
          }
        },
        components:{
          Lunbo02
        },
        methods:{
          xian(){
            this.$router.push("/kefu");
          },
          gwc(){
            this.$router.push("/gouwu");
          },
          xiulian(){
            this.$router.push("/shouye");
          },
          fenx(){
            this.$router.push("/gouwu");
          }
        },
        mounted:function () {
          axios.get('/api/phph0302/zh01.php').then((res)=>{
            this.bol=true;
            this.arr=res.data;
          })
        }
    }
</script>

<style scoped>
*{margin: 0;padding: 0;}
.wrap{
  width: 100%;
  height: 100%;background-color: #f2f2f2}
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
  margin-right: 1rem;
  position: absolute;
  right: 7rem;
}
.gouwu{
  width: 3.8rem;
  height: 3.6rem;
  margin-top:3.7rem;
  position: absolute;
  right: 14rem;
}
.zhuye{
  position: absolute;
  right: 2rem;
  width: 3.8rem;
  height: 3.6rem;
  margin-top:3.7rem;
}
.top span{font-size: 3.6rem;margin-top: 3.2rem;margin-left: 12rem;color: white;
}
.right{
  position: relative;
  width: 15rem;
  height: 4rem;
}
.one{
  width: 100%;
  height: 45.5rem;
  border-top: 1px solid red;
  border-bottom: 1px solid #cccccc;
  margin-top: 3rem;
  background-color: white;
}
.one1 img{
  width: 4rem;
  height: 3rem;
  margin-left: -25rem;
  margin-top: 2rem;
}
  .sp1{
  font-size: 3rem;
  color: #e53e42;
   margin-left: 3rem;
}
.sp2 {
  font-size: 3rem;
    color: #333333;
  margin-left: 2.3rem;
}
  .p1 {
  font-size: 3.6rem;
  color: #e53e42;
    margin-left: -55rem;
    margin-top: 5rem;
}
.sp3{
  font-size: 2.4rem;
  color: #4d4d4d;
  margin-left: -45rem;
  margin-top: 3.4rem;
}
.sp4 {
  display: inline-block;
  width: 7rem;
  height: 2.4rem;
  border-radius: 0.2rem;
  text-align: center;
  line-height: 2.4rem;
  border: solid 1px #e53e42;
  color: #e53e42;
  font-size: 1.6rem;
  margin-left: 1.5rem;
}
  .p2{
    margin-left: -53rem;
  font-size: 2.4rem;
  color: #4d4d4d;
}
  .one2 {
    width: 100%;
    height: 6rem;
    background-color: #ffffff;
    border-top: 1px #cccccc solid;
    border-bottom: 1px #cccccc solid;
}
.jifen{
  display: inline-block;
  margin-left: -18rem;
  margin-top: 1rem;
  font-size: 2.4rem;
  color:red;
}
 .aa{
   display: inline-block;
   margin-left: 4rem;
   font-size: 2.4rem;
 }
.one3{
  width: 100%;
  height: 6.3rem;
  border-bottom: 1px #cccccc solid;
  position: relative;
}
.img1{
  width: 3rem;
  height: 3rem;
  margin-top: 1.5rem;
  margin-left: 10rem;
  vertical-align: center;
}
.img1:nth-child(1){
  margin-left: 0rem;
}
 .one3 span{
   display: inline-block;
   font-size: 2rem;
 }
.you{
  width: 1.4rem;
  height: 2.5rem;
  position: absolute;
  right: 1.2rem;
  top: 2.5rem;
}
.one4{
  position: relative;
  height: 10.2rem;
}
.one4 img{
  width: 4rem;
  height: 3rem;
  margin:2rem 2rem;
  vertical-align: top;
}
  .one4 span{
    margin-top: 2rem;
    display: inline-block;
    width: 60rem;
    height: 5.5rem;
    font-size: 2.4rem;
    line-height: 3.1rem;
    color: #e53e42;
  }
.one4 span:nth-child(3){
  margin-left: -25rem;
  margin-top: -2rem;
}
  .tj {
  width: 8rem;
  height: 3rem;
  background-color: #ffffff;
  border-radius: 2px;
    font-size: 1.8rem;
    color: red;
  border: solid 1px #e53e42;
    position: absolute;
    right: 2rem;
    top: 6rem;
}
  .two{
    margin-top: 2rem;
    background-color: white;
    position: relative;
    height: 24.2rem;
    padding-top: 5rem;
  }
  .two p{
    position: absolute;
    left: 5rem;
    top: 20rem;
    font-size: 2.4rem;
  }
.logo{
  display: inline-block;
  width: 12rem;
  height: 12rem;
  margin: 2rem 2rem;
  border-radius: 50%;
  border: 1px #cccccc solid;
  line-height: 12rem;
  text-align: center;
  font-size: 1.8rem;
  }
.three{
  background-color: white;
  margin-top: 1rem;
  height: 56.2rem;
  text-align: left;
}
.three h2{
  font-size: 2.8rem;
  margin-left: 1.8rem;
  padding-top: 2rem;
}
.three p{
  font-size: 2.4rem;
  padding-top: 2rem;
}
.four{
  width: 100%;
  height: 20rem;
  background-color: white;
  margin-top: 1rem;
  position: relative;
  text-align: center;
  display: flex;
  justify-content: space-around;

}
  .xian1,.xian2{
  width: 21rem;
  height: 2px;
  background-color: #808080;
  display: inline-block;
   position: absolute;
  }
.xian1{top:3.5rem;left: 6rem;}
.xian2{top:3.5rem;right: 6rem;}
  .pinpai{
    font-size: 3rem;
    position: absolute;
    top: 1.7rem;
    left: 30rem;
  }
  .four1{
    margin-top: 7rem;
  }
  .four2{
    margin-top: 8rem;
  }
  .four1 img{
    width: 6rem;
    height: 6rem;
  }
  .four1 span,.four2 span{
    display: inline-block;
    margin-top: 2rem;
    font-size: 1.8rem;
  }
.four2 span{
  margin-top: 3.5rem;
}
  .four2 img{
    width: 8.2rem;
    height: 3.2rem;
  }
  .five{
    width: 100%;
    background-color: #f2f2f2;
    text-align: left;
    height: 58.6rem;
  }
  .five1{
    width: 67.3rem;
    background-color: #f2f2f2;
    position: relative;
  }
  .five1 img{
    position: absolute;
    left: 9rem;
    width: 54rem;
    height: 5.7rem;
    margin-top: 1rem;
  }
  .five1 span{
    margin-left: 2rem;
    display: inline-block;
    font-size: 2.8rem;
    margin-top: 10rem;
  }
  .six{
    width: 100%;
    background-color: white;
    margin-top: 1rem;
    display: flex;
    justify-content:space-around;
    height: 40rem;
    margin-bottom: 8rem;
  }
  .six02,.six03{
    width: 28rem;
    height: 28rem;
    border: 1px #cccccc solid;
    text-align: center;
    margin-top: 7rem;

  }

  .six02 span,.six03 span{
    color: red;
    font-size: 2.4rem;
  }
.six02 p,.six03 p{
  font-size: 2.4rem;
  margin-top: 2rem;
}
  .six02 img,.six03 img{
    width: 14.1rem;
    height: 14.1rem;
    margin-top: 4rem;

  }
  .tuijian02{
    font-size: 3rem;


  }
  .tuijian{
    width: 12rem;
    height: 2.9rem;
    line-height: 2.9rem;
    position: absolute;
    left: 4rem;
    margin-top: 2rem;
  }
  .seven{
    width: 100%;
    height: 1.9rem;
    background-color:#f2f2f2;
    margin-top: 2rem;
    text-align: center;
    line-height: 1.9rem;
  }
.seven span{
color: #808080;
  font-size: 1.8rem;
}
.eight{
  margin-top: 2rem;
  width: 100%;
  height: 9.6rem;
  line-height: 9.6rem;
  text-align: center;
  border-top: 1px dimgray solid;
  position: fixed;
  bottom: 0;
}
.eight span{
  display: inline-block;
  width: 49.7%;
  font-size: 2.8rem;

}
.eight span:nth-child(1),.eight span:nth-child(2){
  background-color: white;
  color: #4d4d4d;
}
.eight span:hover{
  background-color: #f00;
  color: #fff;
}

</style>
