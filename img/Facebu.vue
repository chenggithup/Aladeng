<template>
  <div class="w-w">
    <div v-show="xuan" class="saixuan-w">
      <div class="white-w">
        <div  class="fahuo-w1 fahuo-w">
          <p><img src="../../static/tuijian/fahuodi.png" alt=""></p>
          <div @click="bianhong($event)" class="hui-w1" v-for="item in arr1"><img src="../../static/tuijian/duihao.png" alt=""><p>{{item}}</p></div>
        </div>
        <div  class="fahuo-w2 fahuo-w">
          <p><img src="../../static/tuijian/shangpintype.png" alt=""></p>
          <div @click="bianhong($event)" class="hui-w2" v-for="item in arr2"><img src="../../static/tuijian/duihao.png" alt=""><p>{{item}}</p></div>
        </div>
        <div class="fahuo-w3 fahuo-w">
          <p><img src="../../static/tuijian/chanpinfenlei.png" alt=""></p>
          <div @click="bianhong($event)" class="hui-w3" v-for="item in arr3"><img src="../../static/tuijian/duihao.png" alt=""><p>{{item}}</p></div>
          <div @click="xiang" class="hui-w4">更多分类></div>
        </div>
        <div class="foot-w">
          <div  class="chong-w">重置</div>
          <div @click="saixuan" class="sure-w">确定</div>
        </div>
      </div>
    </div>
    <div v-show="fen" class="saixuan-w">
      <div class="white-w">
        <div class="head-w">
          <img @click="fanhui" src="../../static/tuijian/heijiantou.png" alt="">
          <p class="lei-w">分类</p>
          <p @click="fanaa" class="ding-w">确定</p>
        </div>
        <p class="fenxiang" v-for="item in arr3">{{item}}<img src="../../static/shopping/Hduihao.png" alt=""></p>
      </div>
    </div>
    <div class="head">
    <router-link to="./aa"><img class="ala" src="../../static/tuijian/zuojiantou.png" alt=""></router-link>
    <!--<div class="input"><input   type="text"   class="inp" placeholder="输入商品关键字"></div>-->
    <!--<img class="fd" src="../../static/tuijian/fangdajing.png" alt="">-->
    <span>面部护理</span>

    </div>
    <div class="price-xiao">
      <p>默认</p>
      <p>价格</p>
      <p>销量</p>
      <p @click="saixuan">筛选</p>
    </div>
    <div class="cuncai">
      <img src="../../static/tuijian/shangpin2.png" alt="">
      <div class="jieshao">
        <p class="huancai">焕彩萃璨花蕊唇彩4.8g</p>
        <p class="xiaop">焕彩萃璨花蕊唇彩4.8g焕彩萃璨花蕊唇彩4.8g</p>
        <p class="xiaop">焕彩萃璨花蕊唇彩4.8g</p>
        <p class="bao-you">
          <img class="eng" src="../../static/people/yingguotubiao.png" alt="">
          <img class="feiji" src="../../static/shopping/feiji.png" alt="">
          <span class="hai-wai">海外直邮</span>
          <span class="money">¥166.06</span>
        </p>
      </div>
    </div>
    <div class="cuncai aa">
      <img src="../../static/tuijian/shangpin2.png" alt="">
      <div class="jieshao">
        <p class="huancai">焕彩萃璨花蕊唇彩4.8g</p>
        <p class="xiaop">焕彩萃璨花蕊唇彩4.8g焕彩萃璨花蕊唇彩4.8g</p>
        <p class="xiaop">焕彩萃璨花蕊唇彩4.8g</p>
        <p class="bao-you">
          <img class="eng" src="../../static/people/yingguotubiao.png" alt="">
          <img class="feiji" src="../../static/shopping/feiji.png" alt="">
          <span class="hai-wai">海外直邮</span>
          <span class="money">¥166.06</span>
        </p>
      </div>
    </div>
    <div class="cuncai aa">
      <img src="../../static/tuijian/shangpin2.png" alt="">
      <div class="jieshao">
        <p class="huancai">焕彩萃璨花蕊唇彩4.8g</p>
        <p class="xiaop">焕彩萃璨花蕊唇彩4.8g焕彩萃璨花蕊唇彩4.8g</p>
        <p class="xiaop">焕彩萃璨花蕊唇彩4.8g</p>
        <p class="bao-you">
          <img class="eng" src="../../static/people/yingguotubiao.png" alt="">
          <img class="feiji" src="../../static/shopping/feiji.png" alt="">
          <span class="hai-wai">海外直邮</span>
          <span class="money">¥166.06</span>
        </p>
      </div>
    </div>
    <div class="cuncai aa">
      <img src="../../static/tuijian/shangpin2.png" alt="">
      <div class="jieshao">
        <p class="huancai">焕彩萃璨花蕊唇彩4.8g</p>
        <p class="xiaop">焕彩萃璨花蕊唇彩4.8g焕彩萃璨花蕊唇彩4.8g</p>
        <p class="xiaop">焕彩萃璨花蕊唇彩4.8g</p>
        <p class="bao-you">
          <img class="eng" src="../../static/people/yingguotubiao.png" alt="">
          <img class="feiji" src="../../static/shopping/feiji.png" alt="">
          <span class="hai-wai">海外直邮</span>
          <span class="money">¥166.06</span>
        </p>
      </div>
    </div>
    <div class="im-g aa">
      <img src="../../static/tuijian/lunboImg.png" alt="">
      <p class="jia-zai">加载更多</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Faceli",
    data(){
      return {
        arr1:['小日本','美利坚','大中国','澳大利亚','英国'],
        arr2:['促销商品','收发商品'],
        arr3:[
          '界面护理','人气口红','名牌包包',
          '界面护理','人气口红','名牌包包',
          '界面护理','人气口红','名牌包包',
          '界面护理','人气口红','名牌包包',
          '界面护理','人气口红','名牌包包',
          '界面护理','人气口红','名牌包包',
          '界面护理','人气口红'
        ],
        xuan:false,
        fen:false


      }

    },
    methods:{
       bianhong(e){
         // e.target.style.backgroundColor="#ffd3d3";
         // e.target.style.color="red";
         //e.target.children("img").style.opacity = 1;

       },
      saixuan(){
         this.xuan = !this.xuan
      },
      xiang(){
         this.fen = !this.fen;
        this.xuan = !this.xuan
      },
      fanhui(){
        this.xuan = !this.xuan;
        this.fen = !this.fen
      },
      fanaa(){
         this.$router.push('/aa')
      }
    },
    mounted(){
      $(function () {
        $('.hui-w1').click(function () {
          // $('.hui-w>img').css("opacity","1");
          $('.hui-w1 img').eq($(this).index()-1).css('opacity','1');
          $('.hui-w1 p').eq($(this).index()-1).css({
            backgroundColor:"#ffd3d3",
            color:"#e53e42"
          });
          // $('.hui-w1').eq($(this).index()-1).css('backgroundColor','ffd3d3');
        });
        $('.hui-w2').click(function () {
          // $('.hui-w>img').css("opacity","1");
          $('.hui-w2 img').eq($(this).index()-1).css('opacity','1');
          $('.hui-w2 p').eq($(this).index()-1).css({
            backgroundColor:"#ffd3d3",
            color:"#e53e42"
          });
          // $('.hui-w2').eq($(this).index()-1).css('backgroundColor','ffd3d3');
        });
        $('.hui-w3').click(function () {
          // $('.hui-w>img').css("opacity","1");
          $('.hui-w3 img').eq($(this).index()-1).css('opacity','1');
          $('.hui-w3 p').eq($(this).index()-1).css({
            backgroundColor:"#ffd3d3",
            color:"#e53e42"
          });
          // $('.hui-w3').eq($(this).index()-1).css('backgroundColor','ffd3d3');
        });
        $('.chong-w').click(function () {
          $('.hui-w1 img').css('opacity','0');
          $('.hui-w2 img').css('opacity','0');
          $('.hui-w3 img').css('opacity','0');
          $('.hui-w1 p').css({
            backgroundColor:"#f2f2f2",
            color:"#4d4d4d"
          });
          $('.hui-w2 p').css({
            backgroundColor:"#f2f2f2",
            color:"#4d4d4d"
          });
          $('.hui-w3 p').css({
            backgroundColor:"#f2f2f2",
            color:"#4d4d4d"
          });
        });
        $('.fenxiang').click(function () {
          // $('.hui-w>img').css("opacity","1");
          $('.fenxiang img').eq($(this).index() - 1).css('opacity', '1');
          $('.fenxiang ').eq($(this).index() - 1).css({
            // backgroundColor:"#ffd3d3",
            color: "#e53e42"
          });
        })


      })
    }
  }
</script>

<style scoped>

  .w-w{
    background-color: #f2f2f2;
    height: 130rem;
    position: relative;
  }
  .aa{
    margin-top: 2rem;
  }
  .saixuan-w{
    width: 100%;
    height: 152rem;
    position: absolute;
    left: 0;
    top: 0;
    background-color: rgba(0,0,0,0.4);
    z-index: 2;
  }
  .white-w{
    width: 56rem;
    float: right;
    height: 100%;
    background-color: #ffffff;
  }
  .fahuo-w{
    width: 100%;
    margin-top: 2.5rem;
    /*padding-left: 2rem;*/
    border-bottom: 1px solid #808080;
  }
  .fahuo-w img{
    height: 3rem;
    margin-left: 2rem;
  }
  .hui-w1,.hui-w2,.hui-w3{
    width: 16.2rem;
    height: 8rem;
    background-color: #f2f2f2;
    border-radius: 3px;
    float: left;
    margin-top: 2rem;
    margin-left: 2rem;
    position: relative;
  }
  .hui-w4{
    width: 16.2rem;
    height: 8rem;
    /*background-color: #f2f2f2;*/
    /*border-radius: 3px;*/
    float: left;
    margin-top: 2rem;
    margin-left: 2rem;
    text-align: center;
    line-height: 8rem;
    font-size: 2.8rem;
    /*position: relative;*/
  }
  .hui-w1 p,.hui-w2 p,.hui-w3 p{
    width: 100%;
    height: 100%;
    text-align: center;
    line-height: 8rem;
    font-size: 2.8rem;
  }
  .hui-w1 img,.hui-w2 img,.hui-w3 img{
    position: absolute;
    opacity: 0;
    left: -2rem;
    top: 0;
  }
  .foot-w{
    width: 100%;
    height: 10rem;
    margin-top: 9rem;

  }
  .chong-w,.sure-w{
    width: 50%;
    height: 100%;
    float: left;
    text-align: center;
    line-height: 9rem;
    font-size: 3rem;
  }
  .chong-w{
    background-color: #f2f2f2;
  }
  .sure-w{
    background-color: #e53e42;
    color: white;
  }
  .fahuo-w1{

    height: 26rem;

  }
  .fahuo-w2{

    height: 18rem;

  }
  .fahuo-w3{

    height: 77.7rem;

  }
  .head-w{
    width: 100%;
    height: 9.6rem;
    background-color: #f2f2f2;
    position: relative;
  }
  .head-w img{
    height: 4rem;
    position: absolute;
    top: 3rem;
    left: 2rem;
  }
  .lei-w{
    /*display: inline-block;*/
    font-size: 3.6rem;
    position: absolute;
    color: #696969;
    left: 24rem;
    top: 2rem;
  }
  .ding-w{
    font-size: 3rem;
    position: absolute;
    color: #696969;
    right: 2rem;
    top: 2.5rem;
  }
  .fenxiang{
    width: 52rem;
    height: 6.3rem;
    margin-left: 2rem;
    border-bottom: 1px solid #696969;
    line-height: 6.3rem;
    font-size: 2.8rem;
    color: #696969;
  }
  .fenxiang img{
    float: right;
    width: 2.8rem;
    margin-top: 2rem;
    opacity: 0;
  }
  .head{
    width: 100%;
    height: 9.5rem;
    background-color: #e53e42;
    position: relative;
    /*line-height: 9.5rem;*/
    /*position: fixed;*/
    top: 0;
    left: 0;
    z-index: 1;
  }
  .ala{
    width: 2.6rem;
    height: 4.5rem;
    position: absolute;
    left: 2rem;
    top: 3rem;
  }
  .input {
    width: 53rem;
    height: 5rem;
    /*text-align: center;*/
    /*color: #e53e42;*/
    position: absolute;
    left: 7rem;
    top: 2.5rem;
    border-radius: 1rem;
    line-height: 5rem;
    background-color: white;
  }
  .inp{
    margin-left: 4rem;
    font-size: 3rem;
  }
  input::-webkit-input-placeholder {
    /* placeholder颜色  */
    color: #e53e42;
    /* placeholder字体大小  */
    /*font-size: 3rem;*/
    /* placeholder位置  */
    /*text-align: left; */

  }
  .fd{
    width: 3rem;
    height: 4em;
    position: absolute;
    left: 7.5rem;
    top: 3.5rem;
  }
  .head span{
    font-size: 3.5rem;
    display: block;
    color: white;
    position: absolute;
    right: 28rem;
    top: 2.5rem;
  }
  .price-xiao{
    width: 100%;
    height: 8rem;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: white;

  }
  .price-xiao p{
    font-size: 2.8rem;
    color: #808080;
  }
  .price-xiao p:hover{
    color: #e53e42;
  }
  .cuncai{
    width: 100%;
    height: 22rem;
    background-color: white;
    position: relative;
    border-bottom: 2px solid #696969;
    /*padding-bottom: 2rem;*/
  }
  .cuncai>img{
    position: absolute;
    width: 10rem;
    height: 17.8rem;
    left: 5rem;
    top: 2rem;
  }
  .jieshao{
    width: 48rem;
    height: 17.8rem;
    position: absolute;
    left: 22rem;
    top: 2rem;

  }
  .huancai{
    color: #696969;
    font-size: 3rem;
    margin-bottom: 1rem;
  }
  .xiaop{
    margin-top: 0.5rem;
    color: #808080;
    font-size: 2.2rem;
  }
  .bao-you{
    margin-top: 1rem;
  }
  .eng{
    width: 3.7rem;
    height: 3.2rem;
  }
  .feiji{
    width: 4.2rem;
    height: 4.2rem;
    margin-left: 1.5rem;
    margin-bottom: -0.5rem;
    margin-right: 2rem;

  }
  .hai-wai{
    font-size: 2.4rem;
    color: #808080;
  }
  .money{
    color: #e53e42;
    font-size: 3rem;
    float: right;
  }
  .im-g{
    width: 100%;
    height: 37rem;

  }
  .im-g img{
    width: 100%;
    height: 30rem;
  }
  .jia-zai{
    height: 7rem;
    text-align: center;
    line-height: 7rem;
    font-size: 3rem;
    color: #808080;
  }
</style>
