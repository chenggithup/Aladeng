<template>
  <div class="ac">
    <p class="pl" @click="kk()">编辑</p>
    <div class="peisong">
      <span>订单编号:485269676465</span>
      <span>待支付</span>
    </div>
    <ul class="ul1">
      <li class="li2">
        <div class="shangp">
          <img class="om" src="/static/img/wuyanse.png" alt="" @click="jh()">
          <img src="/static/img/01.png" alt="">
          <span class="sp1">会呼吸丝滑蜜粉</span>
          <span class="sp2">规格 : 蜜粉</span>
          <p><span class="sp3">¥166.06</span> ✖️1件</p>
        </div>
      </li>
    </ul>
    <div class="bottom">
      <p>应付:<span>¥166.06</span></p>
      <Ds style="margin-left: 62rem"></Ds>
      <button @click="bn()">去付款</button>
    </div>
    <div class="bb" v-show="bol">
      <img style=" width: 3rem;height: 3rem;margin-right: 60rem;" src="/static/img/wuyanse.png" alt="" @click="jh()" class="om">
      <button @click="de()">删除</button>
    </div>
  </div>
</template>

<script>
  import Ds from '@/components/Ds'
  export default {
    name: "Third",
    data(){
      return{
        bol:false,
        n:0,
        arr:[]
      }
    },
    methods:{
      kk(){
        this.bol=!this.bol;
        document.getElementsByClassName("om")[0].style.display="block";
      },
      jh(){
        this.n++;
        this.arr.push(this.n);
        document.getElementsByClassName("om")[0].src="/static/img/duihao.png";
        document.getElementsByClassName("om")[1].src="/static/img/duihao.png";
        this.$options.methods.de();
      },
      de(){

        if(this.arr.length%2!=0){
          this.bol = false;
          document.getElementsByClassName("bottom")[0].style.display="none";
          document.getElementsByClassName("peisong")[0].style.display="none";
          document.getElementsByClassName("om")[0].parentNode.parentNode.parentNode.removeChild(document.getElementsByClassName("om")[0].parentNode.parentNode);
        }else{
          alert("您未选中任何商品");
        }
      },
      bn(){
        this.$router.push('/jies');
      }

    },
    components:{
      Ds
    }
  }
</script>

<style scoped>
  .ac{
    height: 100%;
    position: relative;

  }
  .ac p{
    position: absolute;
    right: 3rem;
    top: -16.5rem;
    font-size: 3.6rem;
    color: #ffffff;
  }
  .peisong{
    height: 6rem;
    line-height: 6rem;
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
    color: #f00;
  }
  .ul1{
    list-style-type: none;
    background-color: #fff;
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
    position: absolute;
    left: 1rem;
  }
  .shangp img:nth-child(1){
    width: 3rem;
    height: 3rem;
    position: absolute;
    left: -6rem;
    top: 4rem;
    display: none;
  }
  .sp1{
    width: 20rem;
    position: absolute;
    top: 0rem;
    left: 15rem;
    font-size: 2.8rem;
    color: #4d4d4d;
  }
  .sp2{
    position: absolute;
    top: 5rem;
    left: 15rem;
    font-size: 2.4rem;
    color: #666666;
  }
  .shangp p{
    position: absolute;
    left: 15rem;
    top: 10rem;
    font-size: 2.8rem;
    color: #808080;
    width: 18.9rem;
  }
  .sp3{
    font-size: 2.4rem;
    color: red;
    margin-left: -2rem;
  }
  .bottom{
    width: 100%;
    height: 8.8rem;
    position: relative;
    background-color: #fff;
  }
  .bottom p{
    font-size: 2.8rem;
    position: absolute;
    left: -45rem;
    top: 2rem;
    color: #f00;
  }
  .bottom p span{
     font-size: 2.8rem;
     margin-left: 2rem;
     color: #f00;
   }
  .bottom button{
    width: 12.7rem;
    height: 4rem;
    background-color: #f00;
    color: #fff;
    border-radius: 2rem;
    font-size: 2.4rem;
    position: absolute;
    right: 4rem;
    top: 2rem;
  }
  .bb{
    height: 10rem;

    background-color: #fff;
    line-height: 10rem;
    position: relative;
    position: fixed;
    left: 0;
    bottom: 0;
  }

  .bb button{
    width: 12.7rem;
    height: 4rem;
    background-color: #f00;
    color: #fff;
    border-radius: 2rem;
    font-size: 2.4rem;
    float: left;
    margin-left: 55rem;
    margin-top: -7rem;
  }
</style>
