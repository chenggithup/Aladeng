<template>
  <div class="wrap">
    <div class="cc">
      <div class="top">
        <img @click="xiulian()" src="/static/img/fanhui.png" alt="">
        <span>商品详情</span>
        <div class="right">
          <img style="width: 3.8rem;height: 3.6rem;" class="gouwu" src="/static/img/gouwu.png" alt="">

          <img class="fx" @click="fenx()" src="/static/img/fenxiang.png" alt="">
          <img class="zhuye" src="/static/img/shouye.png" alt="">
        </div>
      </div>
      <!--轮播组件-->
      <Lunbo03></Lunbo03>
      <div class="qg">
        <span>还剩100件,再不抢购就没了哦~</span>
      </div>
    </div>
    <div class="pp0"></div>

    <div class="one">
      <div class="one1">
        <img src="/static/img/miziqi.png" alt="">
        <span class="sp1">英国直邮</span> <span class="sp2">焕彩翠璨花蕊唇彩4.8g焕彩翠璨花</span>
        <p class="sp2 pp1">蕊唇彩4.8g焕彩翠璨花蕊唇彩4.8g</p>
        <p class="p1">¥129</p>
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
        <img class="you" src="/static/img/you.png" alt="" @click="di()">
      </div>
      <div class="one4">
        <img src="/static/img/miziqi.png" alt="">
        <span>直邮,下单时需要提供真实姓名和身份证号以及收获地址,</span>
        <span>请去添加并填写这些信息</span>
        <button class="tj">去添加</button>
      </div>
    </div>

    <div class="xinde">
      <div class="shu"></div>
      <span>阿拉粉心得</span>
      <p>查看更多></p>
    </div>

    <div class="jingyan">
      <div>
        <p>颜色涂抹看上去看着很漂亮,棒棒哒</p>
        <img src="/static/img/xinderen.png" alt="">
        <span>霜霜</span>
      </div>
      <div>
        <p>颜色涂抹看上去看着很漂亮,棒棒哒</p>
        <img src="/static/img/xinderen.png" alt="">
        <span>爱美丽</span>
      </div>
      <div>
        <p>颜色涂抹看上去看着很漂亮,棒棒哒</p>
        <img src="/static/img/xinderen.png" alt="">
        <span>爱美丽</span>
      </div>
    </div>

    <div class="pinpai">
      <img src="/static/img/pinpaibiaozhi.png" alt="">
      <span class="span1">品牌名字品牌名字</span>
      <span class="span2">英国最大彩妆品牌</span>
      <button>+关注</button>
      <p>查看<span class="span3">10</span>件商品</p>
      <span class="span4">品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍品牌介绍...</span>
    </div>

    <div class="cm">
      <div>
        <img src="/static/img/01.png" alt="">
        <p>会呼吸丝滑蜜粉</p>
        <span>¥199</span>
      </div>
      <div>
        <img src="/static/img/02.png" alt="">
        <p>BB矿物粉饼9g</p>
        <span>¥299</span>
      </div>
      <div>
        <img src="/static/img/03.png" alt="">
        <p>植萃腮红胭脂</p>
        <span>¥188</span>
      </div>
    </div>

    <div class="xinde">
      <div class="shu"></div>
      <span>商品描述</span>
    </div>
    <div class="miaoshu">
      <p>该模块主要来实现差几分地阿芳蠢得死胡扯比读书进口车的十年间看出你还是大家看好你参加考试的河南健康才收到货你就看吧发到空间发的你看见你看见的女会计的妇女看见你发的空军奶粉是就大V快递反馈是看到发红包今飞凯达接口的</p>
    </div>

    <div class="xinde" style="margin-top: -2rem">
      <div class="shu"></div>
      <span>使用方法</span>
    </div>
    <div class="miaoshu">
      <p>
        1.该模块主要来实现差比读书<br />
        2.看出你还是大家看好你参加考试的河南健康<br />
        3.你就看吧发到空间</p>
    </div>
    <div class="xinde" style="margin-top: -2rem">
      <div class="shu"></div>
      <span>商品图片</span>
    </div>
    <div class="miaoshu">
      <p style="border-bottom: 0">该模块主要来实现差几分地阿芳蠢得死胡扯比读书进口车的十年间看出你还是大家看好你参加考试的河南健康才收到货你就看吧发到空间发的你看见你看见的</p>
      <div><img src="/static/img/chuncai.png" alt=""></div>
      <div><img src="/static/img/chuncai.png" alt=""></div>
    </div>

    <div class="xinde">
      <div class="shu"></div>
      <span>阿拉粉在买</span>
    </div>
    <div class="cm">
      <div>
        <img src="/static/img/01.png" alt="">
        <p>会呼吸丝滑蜜粉</p>
        <span>¥199</span>
      </div>
      <div>
        <img src="/static/img/02.png" alt="">
        <p>BB矿物粉饼9g</p>
        <span>¥299</span>
      </div>
      <div>
        <img src="/static/img/03.png" alt="">
        <p>植萃腮红胭脂</p>
        <span>¥188</span>
      </div>
    </div>
    <div class="xinde">
      <div class="shu"></div>
      <span>服务承诺</span>
    </div>
    <div class="four" style="margin-top: -1rem;border-top: 1px solid #ccc">

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
        <img src="/static/img/ff.png" alt=""><br>
        <p>野生蓝莓果汁饮料</p>
        <span>¥ 100</span>
      </div>
      <div class="six03">
        <img src="/static/img/hetao.png" alt=""><br>
        <p>原生坚果</p>
        <span>¥ 99</span>
      </div>
    </div>

    <div class="seven">
      <span>继续拖动查看图片详情</span>
    </div>

    <div class="eight">
      <span>在线客服</span> <span>加入购物车</span>
    </div>

    <div class="fuwu">
      <div class="fu">
        <p>服务说明</p>
        <img src="/static/img/chahao.png" alt="" @click="ji()">
      </div>
      <div class="tuihuo">
        <img src="/static/img/buzhichi.png" alt="">
        <span>不支持7天无忧退货</span><br>
        <span>该商品特殊性,一经售出不存在质量问题不享受7天无理由退换</span>
      </div>
      <div class="haiwai">
        <img src="/static/img/zhiyou.png" alt="">
        <span>海外直邮</span><br>
        <span>下单后7~10个工作日发货,发货后平均12-20个工作日到货</span>
      </div>
      <div class="zhengpin">
        <img src="/static/img/zheng.png" alt="">
        <span>正品保证</span><br>
        <span>本商品绝对正品保证</span>
      </div>
    </div>

  </div>

</template>

<script>
  import Lunbo03 from '@/components/Lunbo03'
  import index from "../router";
  export default {
    name: "Spin",
    methods:{
      xiulian(){
        this.$router.push("/shouye");
      },
      di(){
        document.getElementsByClassName("fuwu")[0].style.display="block";
        document.getElementsByClassName("cc")[0].style.opacity="0.1";
        document.getElementsByClassName("pp0")[0].style.webkitZIndex="100";
      },
      ji(){
        document.getElementsByClassName("fuwu")[0].style.display="none";
        document.getElementsByClassName("cc")[0].style.opacity="1";
        document.getElementsByClassName("pp0")[0].style.webkitZIndex="-1";
      }
    },
    components:{
      Lunbo03
    }
  }
</script>

<style scoped>
  .pp0{
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 63rem;
    background-color: rgba(0,0,0,0.01);
    z-index: -1;
  }
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
  .qg{
    width: 100%;
    height: 10rem;
    line-height: 10rem;
    background-color: #f00;
    color: #fff;
    text-align: left;
    margin-top: 3rem;
  }
  .qg span:first-child{
    margin-left: 1.5rem;
    font-size: 3rem;
  }
  .qg span:nth-child(2){
    margin-left: 10rem;
    font-size: 2.4rem;
  }
  .qg button{
    width: 12.4rem;
    height: 4rem;
    border-radius: 2rem;
    background-color: #fff;
    font-size: 2.4rem;
    color: #f00;
    margin-left: 3rem;
  }
  .one{
    width: 100%;
    height: 45.5rem;
    border-top: 1px solid red;
    border-bottom: 1px solid #cccccc;
    background-color: white;
    padding-bottom: 5rem;
  }
  .one1 img{
    width: 4rem;
    height: 3rem;
    margin-top: 2rem;
  }
  .sp1{
    font-size: 3rem;
    color: #e53e42;
    margin-left: 1rem;
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
    margin-top: 1rem;
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
  .pp1{
    margin-left: -10rem;
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
  .xinde{
    margin-top: 2rem;
    background-color: #fff;
    position: relative;
    height: 6rem;
    border-bottom: 1px solid #ccc;
    padding-bottom: 2rem;
  }
  .shu{
    width: 0.5rem;
    height: 3rem;
    background-color: #f00;
    position: absolute;
    left: 2rem;
    top: 2rem;
  }
  .xinde span{
    font-size: 3rem;
    position: absolute;
    left: 3rem;
    top: 1.5rem;
  }
  .xinde p{
    position: absolute;
    right: 2rem;
    top: 2rem;
    font-size: 2rem;
  }
  .jingyan{
    padding-top: 2rem;
    width: 100%;
    display: flex;
    justify-content: space-around;
    background-color: #fff;
  }
  .jingyan div{
    border: 1px solid #ccc;
    text-align: left;
    margin-left: 2rem;
    width: 22.1rem;
    height: 20.1rem;
    border-radius: 1rem;
    padding-bottom: 2rem;
  }
  .jingyan p{
    padding: 1rem;
    margin-top: 2rem;
    font-size: 2.4rem;
  }
  .jingyan img{
    width: 4rem;
    height: 4rem;
    padding-top: 6rem;
    padding-left: 2rem;
    vertical-align: bottom;
  }
  .jingyan span{
    font-size: 1.8rem;
    margin-left: 1rem;
  }
  .pinpai{
    margin-top: 2rem;
    background-color: #fff;
    position: relative;
    height: 20.4rem;
    width: 100%;
    border-bottom: 1px solid #ccc;
  }
  .pinpai img{
    width: 6rem;
    height: 6rem;
    position: absolute;
    left: 2rem;
    top: 2rem;
  }
  .pinpai .span1{
    font-size: 2.8rem;
    position: absolute;
    left: 9rem;
    top: 2rem;

  }
  .span2{
    position: absolute;
    left: 33.3rem;
    top: 2rem;
    font-size: 2rem;
  }
  .pinpai button{
    width: 10rem;
    height: 3rem;
    position: absolute;
    right: 2rem;
    top: 2rem;
    border-radius: 2rem;
    font-size: 2rem;
    border: 1px solid #f00;
    color: #f00;
    background-color: #fff;
  }
  .pinpai p{
    position: absolute;
    left: 9rem;
    top: 5.5rem;
    font-size: 2rem;
  }
  .pinpai .span3{
    color: #f00;
  }
  .pinpai .span4{
    font-size: 1.8rem;
    position: absolute;
    left: 2rem;
    top: 10rem;
  }
  .cm{
    padding-top: 4rem;
    display: flex;
    justify-content: space-around;
    background-color: #fff;
    padding-bottom: 4rem;
  }
  .cm div:nth-child(2) img{
    width: 10.2rem;
    height: 20rem;
    margin-top: -2rem;
  }
  .cm img:first-child{
    width: 12rem;
    height: 14rem;
  }
  .cm div:nth-child(3) img{
    width: 16rem;
    height: 13.9rem;
  }
  .cm p{
    font-size: 2.4rem;
    margin-top: 2rem;
  }
  .cm span{
    font-size: 2.4rem;
    color: #f00;
  }
  .cm div:nth-child(2) p{
    margin-top: -2rem;
  }
  .miaoshu{
    background-color: #fff;
    padding-bottom: 2rem;

  }
  .miaoshu p{
    font-size: 2.4rem;
    text-align: left;
    padding: 2rem;
    border-bottom: 1px solid #cccccc;
  }
  .miaoshu img{
    width: 6.9rem;
    height: 15.3rem;
    margin-top: 4rem;
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
  }
  .eight span{
    display: inline-block;
    width: 49.7%;
    font-size: 2.8rem;
  }
  .eight span:nth-child(1){
    background-color: white;
    color: #4d4d4d;
  }
  .eight span:nth-child(2){
    background-color: red;
    color: white;
  }
  .fuwu{
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 60rem;
    background-color: #fff;
    display: none;
  }
  .fu{
    height: 8rem;
    line-height: 8rem;
    border-bottom: 1px solid #cccccc;
  }
  .fu p{
    font-size: 2.8rem;
  }
  .fu img{
    float: right;
    width: 2.4rem;
    height: 2.4rem;
    margin-top: -5rem;
    margin-right: 2rem;
  }
  .tuihuo{
    margin-top: 2rem;
    width: 100%;
    height: 10rem;
    border-bottom: 1px solid #cccccc;
  }
  .tuihuo img{
    width: 3rem;
    height: 3rem;
    margin-left: -40rem;
  }
  .tuihuo span:nth-child(2){
    font-size: 2.8rem;
    color: #f00;
    margin-left: 1rem;
  }
  .tuihuo span:nth-child(4){
    font-size: 2.4rem;
    color: #808080;
    margin-left: 6rem;
  }
  .haiwai{
    margin-top: 2rem;
    width: 100%;
    height: 10rem;
    border-bottom: 1px solid #cccccc;
  }
  .haiwai img{
    width: 3rem;
    height: 3rem;
    margin-left: -52rem;
  }
  .haiwai span:nth-child(2){
    font-size: 2.8rem;
    color: #f00;
    margin-left: 1rem;
  }
  .haiwai span:nth-child(4){
    font-size: 2.4rem;
    color: #808080;
    margin-left: 2rem;
  }
  .zhengpin{
    margin-top: 2rem;
    width: 100%;
    height: 10rem;
  }
  .zhengpin img{
    width: 3rem;
    height: 3rem;
    margin-left: -52rem;
  }
  .zhengpin span:nth-child(2){
    font-size: 2.8rem;
    color: #f00;
    margin-left: 1rem;
  }
  .zhengpin span:nth-child(4){
    font-size: 2.4rem;
    color: #808080;
    margin-left: -38rem;
  }
</style>
