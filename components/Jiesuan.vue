<template>
  <div class="wrap">
    <div class="top">
      <img @click="xiulian()" src="/static/img/fanhui.png" alt="">
      <span>确认订单</span>
    </div>
    <div class="tianjia">
      <img src="/static/img/caitiao.png" alt="">
      <span>李四</span>
      <span>15012340708</span>
      <p>河南省新乡市红旗区南干道与新中大道交叉口B座10楼102室:邮编453000</p>
      <img src="/static/img/xiugaidizhi.png" alt="" @click="xg()">
      <img src="/static/img/caitiao.png" alt="">
    </div>
    <div class="xing">
      <img src="/static/img/xingzu.png" alt="">
      <p>实名认证</p>
      <img src="/static/img/yizhi.png" alt="">
      <span>李四</span>
      <span>4107*************5</span>
      <img src="/static/img/bianji.png" alt="" @click="xg()"><span>编辑</span>
      <img src="/static/img/shanchu.png" alt="" @click="shna()"><span>删除</span>
    </div>

    <div class="haiwai">
      <span>海外直邮订单</span>
      <div class="shangpin">
        <img src="/static/img/01.png" alt="">
        <p>会呼吸丝滑蜜粉</p>
        <p>规格: 蜜粉</p>
        <p class="pm"><span>¥166.06</span> *1件</p>
      </div>

      <div class="shangpin" v-show="bol">
        <img src="/static/img/01.png" alt="">
        <p>会呼吸丝滑蜜粉</p>
        <p>规格: 蜜粉</p>
        <p class="pm"><span>¥166.06</span> *1件</p>
      </div>
      <div class="xia">收起<img src="/static/img/shangjian.png" alt="" @click="jj()"></div>
    </div>

    <div>
      <ul class="price">
        <li>
          <span>商品金额:</span>
          <span>¥332.12</span>
        </li>
        <li>
          <span>订单邮费:</span>
          <span>¥50.00</span>
        </li>
        <li>
          <span>关税:</span>
          <span>¥10</span>
        </li>
        <li>
          <span>订单金额:</span>
          <span>¥392.12</span>
        </li>
      </ul>
    </div>

    <div class="safe">
      <p>安全提醒:<span>付款成功后,阿拉灯不会以付款异常、卡单、系统升级为由联系您.请勿泄露银行卡号、手机验证码,否则会造成钱财的损失.如有疑问请咨询客服,谨防电话诈骗!</span></p>
    </div>

    <div class="peisong">
      <span>配送方式:</span>
      <span>日本直邮</span>
    </div>

    <div class="peisong">
      <span>共2件商品</span>
      <span class="span1">应付:<span>¥392.12</span></span>
    </div>
    <div class="bottom">
      <img src="/static/img/wuyanse.png" alt="" @click="dl()" class="po">
      <p>本人同意并接受<span>《个人委托协议》</span>和<span>《用户协议》</span></p>
      <button @click="ds()">确认</button>
    </div>

  </div>
</template>

<script>
  export default {
    name: "Jiesuan",
    data(){
      return{
        bol:true,
        n:0,
        arr:[]
      }
    },
    methods:{
      xg(){
        this.$router.push('/add2');
      },
      shna(){
        $('.xing').remove();
      },
      jj(){
        this.bol = !this.bol;
      },
      dl(){
        this.n++;
        this.arr.push(this.n);
        if(this.n%2==0){
          document.getElementsByClassName("po")[0].src="/static/img/wuyanse.png"
        }else{
          document.getElementsByClassName("po")[0].src="/static/img/duihao.png";
        }

      },
      ds(){
        if(this.arr.length%2!=0){
          this.$router.push('/jies');
        }else{
          alert('404');
        }
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
    height: 100%;
    background-color: #f2f2f2;
  }
  .top{
    background-color: red;
    height: 11.3rem;
    width: 100%;
    text-align: center;
    line-height: 11.3rem;
  }
  .top img{
    width: 2.3rem;
    height: 3.8rem;
    margin-top:3.7rem;
    float: left;
    margin-left: 4rem;
  }
  .top span{
    font-size: 3.6rem;
    margin-top: 3.2rem;
    margin-left: -4rem;
    color: white;
  }
  .tianjia{
    width: 100%;
    margin-top: 2rem;
    position: relative;
  }
  .tianjia img{
    width: 100%;
  }
  .tianjia span:nth-child(2){
    font-size: 2.8rem;
    position: absolute;
    left: 2rem;
    top: 2rem;
  }
  .tianjia span:nth-child(3){
    font-size: 2.8rem;
    position: absolute;
    left: 15rem;
    top: 2rem;
  }
  .tianjia img:nth-child(2){
    width: 4.8rem;
    height: 4.8rem;
    float: left;
    margin-left: 2rem;
    padding: 2rem;
  }
  .tianjia p{
    width: 43rem;
    font-size: 2.4rem;
    color: #808080;
    float: left;
    margin-left: 2rem;
    margin-top: 6rem;
    text-align: left;
    padding-bottom: 2rem;
  }
  .tianjia img:nth-child(5){
    width: 8.2rem;
    height: 8.2rem;
    position: absolute;
    right: 2rem;
    top: 5rem;
  }
  .xing{
    width: 100%;
    background-color: #fff;
    margin-top: 2rem;
    margin-bottom: 2rem;
    position: relative;
    height: 17.8rem;
  }
  .xing p:nth-child(2){
    position: absolute;
    left: 2rem;
    top: 2rem;
    font-size: 3rem;
  }
  .xing img:nth-child(3){
     position: absolute;
     left: 15rem;
     top: 2rem;
     width: 39.6rem;
     height: 4rem;
   }
  .xing span:nth-child(4){
    position: absolute;
    left: 2rem;
    top: 10rem;
    font-size: 2.8rem;
  }
  .xing span:nth-child(5){
    position: absolute;
    left: 15rem;
    top: 10rem;
    font-size: 2.8rem;
  }
  .xing img{
    width: 100%;
    height: 100%;
  }
  .xing img:nth-child(6){
    width: 3rem;
    height: 3rem;
    position: absolute;
    right: 20rem;
    bottom: 2rem;
  }
  .xing span:nth-child(7){
    position: absolute;
    right: 15rem;
    bottom: 2rem;
    font-size: 2.4rem;
  }
  .xing img:nth-child(8){
    width: 3rem;
    height: 3rem;
    position: absolute;
    right: 10rem;
    bottom: 2rem;
  }
  .xing span:nth-child(9){
    position: absolute;
    right: 5rem;
    bottom: 2rem;
    font-size: 2.4rem;
  }
  .haiwai{
    width: 100%;
    background-color: #fff;
  }
  .haiwai span{
    font-size: 2.8rem;
    float: left;
    margin-left: 2rem;
    height: 8rem;
    line-height: 8rem;
  }
  .haiwai .shangpin{
    clear: both;
    border-top: 1px solid #ccc;
    border-bottom: 1px solid #ccc;
    overflow: hidden;
    position: relative;
  }
  .shangpin img{
    width: 12rem;
    height: 14rem;
    float: left;
    padding: 6rem;
    margin-left: 4rem;
  }
  .shangpin p:nth-child(2){
    font-size: 2.8rem;
    position: absolute;
    left: 28rem;
    top: 4rem;
  }
  .shangpin p:nth-child(3){
    font-size: 2.4rem;
    position: absolute;
    left: 28rem;
    top: 10rem;
  }
  .pm{
    font-size: 2.8rem;
    position: absolute;
    left: 40rem;
    top: 18rem;
    color: #808080;
  }
  .pm span{
    font-size: 2.4rem;
    position: absolute;
    left: -14rem;
    top: -2rem;
    color: #f00;
  }
  .xia{
    font-size: 2.8rem;
    padding: 2rem;
  }
  .xia img{
    width: 2.5rem;
    height: 1.4rem;
    margin-left: 1rem;
  }
  .price{
    width: 100%;
    height: 24.4rem;
    margin-top: 2rem;
    background-color: #fff;
    border-bottom: 1px solid #ccc;
  }
  .price li{
    height: 6.1rem;
    line-height: 6.1rem;
    border-bottom: 1px solid #ccc;
  }
  .price li span:first-child{
    float: left;
    font-size: 2.8rem;
    margin-left: 2rem;
  }
  .price li span:last-child{
    float: right;
    font-size: 2.4rem;
    color: #f00;
    margin-right: 2rem;
  }
  .safe{
    width: 100%;
    text-align: left;
    position: relative;
    height: 13.6rem;
    background-color: #fff;
    padding-bottom: 2rem;
  }
  .safe p{
    position: absolute;
    font-size: 2.8rem;
    color:#f00;
    left: 0;
    top: 0;
    padding: 2rem;
  }
  .safe p span{
    font-size: 2.4rem;
    color: #666666;
  }
  .peisong{
    height: 6rem;
    line-height: 6rem;
    margin-top: 2rem;
    background-color: #fff;
    border-bottom: 1px solid #ccc;
  }
  .peisong span:first-child{
    font-size: 2.8rem;
    float: left;
    margin-left: 2rem;
  }
  .peisong span:last-child{
    font-size: 2.8rem;
    float: right;
    margin-right: 2rem;
  }
  .span1 span{
    color: #f00;
  }
  .bottom{
    width: 100%;
    height: 16.2rem;
    position: relative;
    background-color: #fff;
  }
  .bottom img{
    background-color: #fff;
    width: 3rem;
    height: 3rem;
    float: left;
    margin-left: 4rem;
    margin-top: 2rem;
    vertical-align: bottom;
  }
  .bottom p{
    font-size: 2.8rem;
    position: absolute;
    left: 8rem;
    top: 2rem;
  }
  .bottom p span{
    color: #f00;
  }
  .bottom button{
    width: 68rem;
    height: 4rem;
    background-color: #f00;
    border-radius: 2rem;
    margin-top: 4rem;
    font-size: 2.8rem;
    color: #fff;
  }
</style>
