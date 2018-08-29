<template>
  <div v-if="bol" class="ch">
    <div class="lun">
      <img src="/static/img/xinde.png" alt="">
    </div>
    <div class="center">
      <div class="shang">
        <div>
          <img src="/static/img/ribenzhiyou.png" alt="">
          <p>日本直邮</p>
        </div>
        <div>
          <img src="/static/img/meiguozhiyou.png" alt="">
          <p>美国直邮</p>
        </div>
        <div>
          <img src="/static/img/yingguo.png" alt="">
          <p>英国直邮</p>
        </div>
      </div>
      <div class="xia">
        <div>
          <img src="/static/img/aodaliya.png" alt="">
          <p>澳大直邮</p>
        </div>
        <div>
          <img src="/static/img/zhongguo.png" alt="">
          <p>中国直邮</p>
        </div>
      </div>
    </div>
    <div style="margin-top: 2rem;padding-top: 2rem;border-top: 1px solid gray"><span style=" font-size: 2.8rem;height: 3rem;margin-top: 4rem;margin-left: -40rem">热卖品类</span></div>
    <div class="bottom">
      <div class="remai" v-for="item in arr">
        <router-link to="/pinpai"><img src="/static/img/mingpaibaoabao.png" alt=""></router-link>
        <p>{{arrC[21].names}}</p>
      </div>

    </div>
  </div>
</template>

<script>
  import axios from 'axios'
  export default {
    name: "Ch",
    data(){
      return{
        arr:[1,2,3,4,5,6],
        bol:false,
        arrC:[]
      }
    },
    mounted: function () {
      axios.get('/api/phph0302/zh01.php').then((res)=>{
        this.bol=true;
        this.arrC=res.data;
      })
    }
  }
</script>

<style scoped>
  .ch{
    width: 54rem;
    height: 109rem;
    margin-left: -52rem;
  }
  .lun {
    width: 50.2rem;
    margin-left: 2.2rem;
    margin-top: 1.7rem;
  }
  .ch .lun img{
    width: 50rem;
    height: 20.3rem;
  }
  .center{
    width: 54rem;
  }
  .shang{
    display: flex;
    justify-content: space-around;
  }

  .shang div{
    margin-top: 4rem;
    margin-left: 2rem;
  }
  .xia{
    display: flex;
    justify-content: left;
  }
  .xia div{
    margin-top: 4rem;
    margin-left: 5rem;
  }
  .xia div:last-child{
    margin-left: 6rem;
  }
  .center img{
    width: 5.3rem;
    height: 4.8rem;
  }
  .center div p{
    margin-top: 2rem;
    font-size: 2.8rem;
  }
  .ch .bottom{
    display: flex;
    justify-content: space-around;
    flex-wrap:wrap;
    width: 46rem;
  }

  .remai{
    width: 12rem;
    margin-top:2rem;
    padding-left: 3rem;
  }
  .remai img{
    width: 16rem;
    height: 12rem;
  }
  .remai p{
    font-size: 3rem;
  }
</style>
