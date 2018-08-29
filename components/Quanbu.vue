<template>
    <div class="wrap">
      <div class="tou">
        <img src="/static/img/zuo.png" alt="" @click="bd()">
        <p>全部订单</p>
        <!--<span>编辑</span>-->
      </div>
      <div class="nave">
        <span class="tab" @click="toggleTab('Fifth')">全部订单</span>
        <span class="tab" @click="toggleTab('Third')">待支付</span>
        <span class="tab" @click="toggleTab('First')">待发货</span>
        <span class="tab" @click="toggleTab('Second')">待收货</span>
        <span class="tab" @click="toggleTab('Forth')">交易完成</span>
      </div>
      <div><First :is="currentTab" keep-alive></First></div>


    </div>
</template>

<script>
    import First from '@/components/First'
    import Second from '@/components/Second'
    import Third from '@/components/Third'
    import Forth from '@/components/Forth'
    import Fifth from '@/components/Fifth'
    import Daojishi from '@/components/Daojishi'
    export default {
        name: "Quanbu",
      data () {
        return {
          currentTab: 'First' // currentTab 用于标识当前触发的子组件
        };
      },
        components:{
          Daojishi,
          First,
          Second,
          Third,
          Forth,
          Fifth
        },
        methods: {
         toggleTab: function(tab) {
         this.currentTab = tab; // tab 为当前触发标签页的组件名
        },
          bd(){
           this.$router.push('/geren');
          }
      }
    }

</script>

<style scoped>
  .wrap{
    width: 100%;
    background-color: #f2f2f2;
    overflow-y: scroll;
  }
  .tou{
    width: 100%;
    height: 9.6rem;
    line-height: 9.6rem;
    text-align: center;
    position: relative;
    background-color: #f00;
  }
  .tou p{
    font-size: 3.6rem;
    color: #ffffff;
  }
  /*.tou span{*/
    /*font-size: 3.6rem;*/
    /*position: absolute;*/
    /*right: 3rem;*/
    /*color: #fff;*/
    /*top: 0rem;*/
  /*}*/
  .tou img:nth-child(1){
    width: 2.3rem;
    height: 3.8rem;
    position: absolute;
    left: 2rem;
    top: 3rem;
  }
  .nave{
    width: 100%;
    height: 8rem;
    display: flex;
    justify-content: space-around;
    border-bottom: 1px solid #ccc;
    line-height: 8rem;
    padding-top: 1rem;
    background-color: #fff;
  }
  .nave span{
    font-size: 3rem;
  }
  .nave span:hover{
    color: #e83d41;
    border-bottom: 0.2rem solid #ff0000;
  }



</style>
