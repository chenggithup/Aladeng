<template>
  <div class="wrap">
    <div class="nav">
      <span class="span1">阿拉灯</span>
      <input class="inp" type="text" value="" placeholder="输入商品关键字" @click="dj()">
      <img class="sousuo" src="/static/img/sousuo.png" alt="">
      <img style="width: 3.8rem;height: 3.8rem;position: absolute;right: 2.2rem;top: 3rem;" src="/static/img/xiaoxi.png" alt="" @click="dian()">
    </div>
   <div class="center">
     <div class="zuoce">
       <ul>
         <li class="tab" @click="toggleTab('Haizi')">为您推荐</li>
         <li class="tab" @click="toggleTab('Son')">面部护理</li>
         <li class="tab" @click="toggleTab('Ch')">底妆彩妆</li>
         <li class="tab" @click="toggleTab('Haizi')">休闲零食</li>
         <li class="tab" @click="toggleTab('Son')">身体护理</li>
         <li class="tab" @click="toggleTab('Ch')">美容美发</li>
         <li class="tab" @click="toggleTab('Haizi')">生活用品</li>
         <li class="tab" @click="toggleTab('Son')">个人护理</li>
         <li class="tab" @click="toggleTab('Ch')">保健养生</li>
         <li class="tab" @click="toggleTab('Haizi')">时尚潮品</li>
         <li class="tab" @click="toggleTab('Son')">母婴用品</li>
       </ul>
     </div>
     <div class="right">
       <Haizi :is="currentTab" keep-alive></Haizi>
     </div>
   </div>
    <div class="bottom">
      <div>
        <router-link to="/shouye"><img style="width:4.8rem;height: 4.8rem;" src="/static/img/shouyeqian.png" alt=""></router-link>
        <p>首页</p>
      </div>
      <div>
        <img class="i1" @click="dd()" style="width:4.8rem;height: 4.8rem;" src="/static/img/fenleiqian.png" alt="">
        <p>分类</p>
      </div>
      <div>
        <router-link to="dhuowang"><img style="width:11.3rem;height: 5.5rem;" src="/static/img/duanhuo.png" alt=""></router-link>
      </div>
      <router-link to="/gouwu"><div>
        <img style="width: 5rem;height: 4.8rem;" src="/static/img/gouwuche.png" alt="">
        <p>购物车</p>
      </div></router-link>
      <div>
        <router-link to="dz"><img style="width: 4.3rem;height: 4.8rem;" src="/static/img/geren.png" alt=""></router-link>
        <p>个人中心</p>
      </div>
    </div>
  </div>
</template>

<script>
    import Haizi from '@/components/Haizi'
    import Son from '@/components/Son'
    import Ch from '@/components/Ch'
    export default {
        name: "Fenlei",
        data(){
          return{
            bol:true,
            n:0,
            currentTab: 'Haizi' // currentTab 用于标识当前触发的子组件
          }
        },
        methods:{
          toggleTab: function(tab) {
            this.currentTab = tab; // tab 为当前触发标签页的组件名
          },
          dd(){
            this.n++;
            if(this.n %2 == 0){
              document.getElementsByClassName("i1")[0].src="/static/img/fenleiqian.png";
            }else{
              document.getElementsByClassName("i1")[0].src="/static/img/fenleihou.png";
            }
          },
          dianji(){
            this.$router.push('/hai');
          },
          dian(){
            this.$router.push('/xiaoxi');
          }
        },
      components:{
          Haizi,
          Son,
          Ch
      }
    }
</script>

<style scoped>
  .wrap{
    width: 100%;
    background-color: #f2f2f2;
    overflow-y: scroll;
  }
  .nav{
    background-color: #e53e42;
    width: 100%;
    height: 9.6rem;
    line-height: 9.6rem;
    position: relative;
    /*border: 1px solid black;*/
  }
  .inp{
    width: 40rem;
    height: 5rem;
    border-radius: 1rem;
    font-size: 2.4rem;
    text-align: center;
  }
  .inp::-webkit-input-placeholder {
    /* placeholder颜色  */
    color: #e53e42;
    /* placeholder字体大小  */
    font-size: 2.4rem;
    /* placeholder位置  */
    text-align: center;
  }
  .span1{
    font-size: 3.6rem;
    color: #fff;
    position: absolute;
    left: 2.4rem;
  }
  .sousuo{
    width: 2.8rem;
    height: 3rem;
    position: absolute;
    left: 24.4rem;
    top: 3.3rem;
  }
  .center{
    height: 109rem;
    background-color: #fff;
  }
  .zuoce{
    position: absolute;
    left: -1rem;
    top: 9.6rem;
  }
  .zuoce ul{
    width: 17.7rem;
    height: 109rem;
    border-right: 1px solid black;
  }
  .zuoce ul li{
    width: 17.7rem;
    height: 8.5rem;
    line-height: 8.5rem;
    font-size: 3rem;
    border: 1px solid black;
    border-right: 1px solid black;
  }
  .zuoce ul li:hover{
    color:#f00;
    border-right: 3px solid #f00;
  }

  .bottom{
    position: fixed;
    left: 0;
    bottom: 0;
    background-color: #fff;
    display: flex;
    justify-content: space-around;
    width: 100%;
    height: 9.7rem;
    text-align: center;
    line-height: 9.7rem;
    border-top: 1px solid #e6e6e6;
  }
  .bottom img{
    margin-top: 1.5rem;
  }
  p{
    margin-top: -8rem;
    font-size: 2rem;
  }
  .right{
    float: right;
    width: 54px;
  }
</style>
