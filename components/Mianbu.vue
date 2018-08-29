<template>
  <div class="wrap">
    <div class="top">
      <img @click="ba()" src="/static/img/zuo.png" alt="" class="inp">
      <div>
      </div>
      <div class="mb">
        面部护理
      </div>
    </div>
    <div class="xl">
      <div class="mr">
        销量
      </div>
      <div class="zuixin">
        最新
      </div>
      <div class="price">
        <div class="jiage">
          价格
        </div>
        <img src="/static/img/jiage.png" alt="">
      </div>
      <div class="sx">
        <p @click="kl()">筛选</p>
      </div>
    </div>
    <div class="daigou">
      <div class="dh">
        <img src="/static/img/duihao.png" alt="">
      </div>
      <div class="cc">
        <img src="/static/img/chuncai.png" alt="">
      </div>
      <div class="zb">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="zz">
        焕彩萃璨花蕊唇彩4.8g焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="zx">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="jp">
        <img src="/static/img/xiaoriben.png" alt="">
      </div>
      <div class="fly">
        <img src="/static/img/feiji.png" alt="">
      </div>
      <div class="hw">
        海外直邮
      </div>
      <div class="jia">
        ¥ 166.06
      </div>
    </div>
    <div class="daigou">
      <div class="dh">
        <img src="/static/img/duihao.png" alt="">
      </div>
      <div class="cc">
        <img src="/static/img/chuncai.png" alt="">
      </div>
      <div class="zb">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="zz">
        焕彩萃璨花蕊唇彩4.8g焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="zx">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="jp">
        <img src="/static/img/xiaoriben.png" alt="">
      </div>
      <div class="fly">
        <img src="/static/img/feiji.png" alt="">
      </div>
      <div class="hw">
        海外直邮
      </div>
      <div class="jia">
        ¥ 166.06
      </div>
    </div>
    <div class="daigou">
      <div class="dh">
        <img src="/static/img/duihao.png" alt="">
      </div>
      <div class="cc">
        <img src="/static/img/chuncai.png" alt="">
      </div>
      <div class="zb">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="zz">
        焕彩萃璨花蕊唇彩4.8g焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="zx">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="jp">
        <img src="/static/img/xiaoriben.png" alt="">
      </div>
      <div class="fly">
        <img src="/static/img/feiji.png" alt="">
      </div>
      <div class="hw">
        海外直邮
      </div>
      <div class="jia">
        ¥ 166.06
      </div>
    </div>
    <div class="daigou">
      <div class="dh">
        <img src="/static/img/duihao.png" alt="">
      </div>
      <div class="cc">
        <img src="/static/img/chuncai.png" alt="">
      </div>
      <div class="zb">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="zz">
        焕彩萃璨花蕊唇彩4.8g焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="zx">
        焕彩萃璨花蕊唇彩4.8g
      </div>
      <div class="jp">
        <img src="/static/img/xiaoriben.png" alt="">
      </div>
      <div class="fly">
        <img src="/static/img/feiji.png" alt="">
      </div>
      <div class="hw">
        海外直邮
      </div>
      <div class="jia">
        ¥ 166.06
      </div>
    </div>
    <div class="slider">
      <img src="/static/img/lunbo.png" alt="">
    </div>
    <div class="db">
      加载更多
    </div>

    <div class="right" v-show="bol">
      <div class="sh">
        <img src="/static/img/fahuofdi.png" alt="">
        <span>发货地</span>
        <div class="dizhi">
          <button>日本</button>
          <button>美国</button>
          <button>中国</button>
          <button>澳大利亚</button>
          <button>英国</button>
        </div>
      </div>
      <div class="sh">
        <img src="/static/img/splx.png" alt="">
        <span>商品类型</span>
        <div class="dizhi">
          <button>促销商品</button>
          <button>首发商品</button>
        </div>
      </div>

      <div class="sh">
        <img src="/static/img/fenlei.png" alt="">
        <span>分类</span>
        <div class="dizhi">
          <button>洁面护理</button>
          <button>人气口红</button>
          <button>名牌包包</button>
          <button>洁面护理</button>
          <button>人气口红</button>
          <button>名牌包包</button>
          <button>洁面护理</button>
          <button>人气口红</button>
          <button>名牌包包</button>
          <button>洁面护理</button>
          <button>人气口红</button>
          <button>名牌包包</button>
          <button>洁面护理</button>
          <button>人气口红</button>
          <button>名牌包包</button>
          <button>洁面护理</button>
          <button>人气口红</button>
          <button>名牌包包</button>
          <button>洁面护理</button>
          <button>人气口红</button>
          <button>更多分类></button>
        </div>
      </div>
      <div class="qu">
        <button>重置</button>
        <button>确定</button>
      </div>



    </div>

  </div>
</template>
<script>
  export default {
    name: "Chuncai",
    data(){
      return{
       bol: false
      }
    },
    methods:{
      ba(){
        this.$router.push("/fenlei");
      },
      kl(){
        this.bol=!this.bol;
      }
    }
  }
</script>

<style scoped>
  *{
    margin: 0;
    padding: 0;
  }
  .wrap{
    width: 100%;
    background-color: #f2f2f2;
    position: relative;
    overflow-x: hidden;
  }
  .top{
    display: flex;
    justify-content:space-between;
    background-color: red;
    height: 11.3rem;
    line-height: 11.3rem;
    width: 100%;
  }
  .top img:nth-child(1){
    width: 2.3rem;
    height: 3.8rem;
    margin-top:3.7rem;
    margin-left: 2rem;
  }
  div input placeholder{
    position: absolute;
    font-size: 2.8rem;
    left: 30rem;
  }
  .top div{
    text-align: center;
    width: 54.3rem;
    height: 6rem;
  }
  .top div input{
    position: absolute;
    top: 2.5rem;
    left: 8rem;
    width: 54.3rem;
    height: 6rem;
    border-radius: 1rem;
  }

  .cg img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    left: 56rem;
  }
  .xl{
    position:relative;
    width: 72rem;
    height: 8rem;
    top: 0.1rem;
  }
  .mr{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(229,62,66);
    left: -35rem;
    top: 10rem;
  }
  .zuixin{
    position: absolute;
    font-size: 2.8rem;
    top: 10rem;
    left: -17rem;
  }
  .jiage{
    position: absolute;
    font-size: 2.8rem;
    top: 10rem;
    left: -0.1rem;
  }
  .price img{
    position: absolute;
    width: 0.8rem;
    height: 1.7rem;
    top: 11.5rem;
    left:6rem;
    /*border: 1px solid darkblue;*/
    /*background-color: deeppink;*/
  }
  .xl{
    position: absolute;
    font-size: 2.8rem;
    top: 2rem;
    left: 42rem;
  }
  .sx{
    position: absolute;
    font-size: 2.8rem;
    top: 10rem;
    left: 18rem;

  }
  .daigou{
    position: relative;
    width: 100%;
    height: 20rem;
    border:1px solid gray;
    background-color: #fff;
    margin-top: 6rem;
  }

  .dh img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    top: 8rem;
    left: 1rem;
    opacity: 0;
  }
  .cc img{
    position: absolute;
    width: 6.9rem;
    height:15.3rem;
    top: 2rem;
    left: 7.5rem;
  }
  .zb{
    position: absolute;
    font-size: 3rem;
    color: rgb(51,51,51);
    font-family: SimHei;
    left: 20rem;
    top:1rem;
  }
  .zz{
    position: absolute;
    font-size: 2.4rem;
    color:rgb(77,77,77);
    left: 20rem;
    top: 6rem;
  }
  .zx{
    position: absolute;
    font-size: 2.4rem;
    color:rgb(77,77,77);
    left: 20rem;
    top: 10rem;
  }
  .mb{
     position: absolute;
     font-size: 3rem;
     color: white;
    top: 1rem;
    left: 10rem;
  }
  .jp img{
    position: absolute;
    width: 3rem;
    height: 2rem;
    top: 15.3rem;
    left: 21rem;
  }
  .fly img{
    position: absolute;
    width: 3.4rem;
    height: 3.3rem;
    top: 14.5rem;
    left: 26rem;
  }
  .hw{
    position: absolute;
    font-size: 2.4rem;
    top: 14.5rem;
    left: 30rem;
  }
  .jia{
    position: absolute;
    font-size: 3rem;
    color: rgb(229,62,66);
    top: 15rem;
    left: 58rem;
  }

  .jp3 img{
    position: absolute;
    width: 3rem;
    height: 2rem;
    top: 15.3rem;
    left: 21rem;
  }
  .fly3 img{
    position: absolute;
    width: 3.4rem;
    height: 3.3rem;
    top: 14.5rem;
    left: 26rem;
  }
  .slider{
    margin-top: 2rem;
  }
  .slider img{
    width: 72rem;
    height: 30rem;
  }
  .db{
    font-size: 2.4rem;
    margin-top: 2rem;
    height: 7.3rem;
    line-height: 7.3rem;
    color: grey;
  }
  .right{
    position: absolute;
    right: 0;
    bottom: 0;
    height: 142.9rem;
    width: 56rem;
    background-color: #fff;
  }
  .sh{
    padding-top: 2rem;
    border-bottom: 1px solid #ccc;
    padding-bottom: 2rem;
  }
  .sh img{
    width: 3.4rem;
    height: 3rem;
    margin-left: -35rem;
  }
  .sh span{
    font-size: 3rem;
    margin-left: 2rem;

  }
  .dizhi{
    display: flex;
    flex-wrap: wrap;
    justify-content: left;
  }
  .dizhi button{
    width: 16rem;
    height: 8rem;
    font-size: 2.8rem;
    border-radius: 2rem;
    background-color: #f2f2f2;
    margin-left: 2rem;
    margin-top: 2rem;
  }
  .qu button{
    width: 27.8rem;
    height: 8rem;
    font-size: 2.8rem;
    border-radius: 2rem;
    background-color: #f2f2f2;
    margin-top: 10rem;
    color: #ffffff;
  }
  .qu button:hover{
    background-color: #f00;
  }
  .dizhi button:hover{
    background-color: #f00;
  }
</style>
