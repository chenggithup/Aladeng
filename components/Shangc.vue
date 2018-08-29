<template>

  <div class="wrap">

    <div class="top">
      <img @click="xiulian()" src="/static/img/fanhui.png" alt="">
      <span class="wo">我的商城</span>
      <span class="dnum">神灯值</span>
     <div class="top2">
       <span>100</span>
       <img src="/static/img/niaohu.png" alt="">
     </div>
    </div>
     <div class="inp">
       <input class="inp1" type="text" placeholder="🔍查找你想要的商品">
     </div>

    <div class="tabs">
    <div class="tab" @click="toggleTab('One')">
      <span class="jx">精选</span>
    </div>
    <div class="tab" @click="toggleTab('Two')">
      <span class="jx">面膜</span>
    </div>
    <div class="tab" @click="toggleTab('Three')">
      <span class="jx">母婴</span>
    </div>
    <div class="tab" @click="toggleTab('Four')">
      <span class="jx">美妆</span>
    </div>
    <div class="tab" @click="toggleTab('Five')">
      <span class="jx">眼妆</span>
    </div>
  </div>
    <!-- 子组件，显示不同的 tab-->
    <!-- is 特性动态绑定子组件-->
    <!-- keep-alive 将切换出去的组件保留在内存中-->
    <One :is="currentTab" keep-alive></One>
  </div>
</template>

<script>
  import One from '@/components/One'
  import Two from '@/components/Two'
  import Three from '@/components/Three'
  import Four from '@/components/Four'
  import Five from '@/components/Five'
    export default {
        name: "Shangc",
      data () {
        return {
          currentTab: 'One' // currentTab 用于标识当前触发的子组件
        };
      },
      components: { // 声明子组件
        One,
        Two,
        Three,
        Four,
        Five
      },
      methods: {
        toggleTab: function(tab) {
          this.currentTab = tab; // tab 为当前触发标签页的组件名
        },
        xiulian(){
          this.$router.push('/dz');
        }
      },
      mounted:function () {

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
    background-color:white;
  }
  .top{
    position: relative;
    background-color: red;
    height: 17.2rem;
    width: 100%;

  }
  .top img:nth-child(1){
    width: 2.3rem;
    height: 3.8rem;
    margin-top:3.7rem;
    margin-left: -60rem;
  }
  .wo{font-size: 3.6rem;margin-top: 3.7rem;color: white;position: absolute;left: 28.7rem;}
  .dnum{font-size: 3rem;margin-top: 3.7rem;color: white;margin-right: 2rem;position: absolute;right: 3rem;}
  .top2{
    position: absolute;
    left: 28rem;
    top:11rem;
  }
  .top2 span{
    font-size: 4rem;
    color: #ffd21f;
    padding: 2rem;
  }
  .top2 img{
    width: 4rem;
    height: 2.6rem;
  }
  .inp{
    width: 100%;
    height: 8rem;
    text-align: center;
    line-height: 8rem;
  }
  .inp input{
    width: 68rem;
    height: 4.8rem;
    border-radius: 1rem;
    border: solid 1px #cccccc;
    text-align: center;
  }
  .inp1{
    font-size: 2.4rem;
  }
  .inp1::-webkit-input-placeholder{
    color: red;
  }
.tabs{
     width: 100%;
     height: 8rem;
     background-color: #680a0c;
     display: flex;
     justify-content: space-around;
     line-height: 8rem;

   }
  .tab{
    font-size: 2.8rem;
    color: white;
  }
  .jx:hover{
    color: yellow;
  }
</style>
