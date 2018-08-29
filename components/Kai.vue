<template>
  <div v-if="bol" class="kaishou">
    <p class="ks">即将开售</p>
    <div class="d1"></div>
    <span class="mz">美妆专区</span>
    <div class="d2"></div>
    <div class="repin">
      <div class="img1">
        <img style="width: 12rem;height: 14rem;" :src="arr[6].src" alt="">
        <img style="width: 4rem;height: 7.6rem;" src="/static/img/zi.png" alt="">
        <span>{{arr[6].names}}</span>
        <p class="po1">即将开始</p>
        <p class="po2"><Ds style="font-size: 1.5rem;margin-left: 5rem;"></Ds></p>
      </div>

      <div class="img1">
        <img style="width: 10.2rem;height: 20rem;top: 7%;" :src="arr[7].src" alt="">
        <img style="width: 4rem;height: 7.6rem;" src="/static/img/zi.png" alt="">
        <span>{{arr[7].names}}</span>
        <p class="po1">即将开始</p>
        <p class="po2"><Ds style="font-size: 1.5rem;margin-left: 5rem;"></Ds></p>
      </div>
      <div class="img1"><img style="width: 16rem;height: 13.9rem;top: 15%;left: 10%;" :src="arr[8].src" alt="">
        <img style="width: 4rem;height: 7.6rem;" src="/static/img/zi.png" alt="">
        <span>{{arr[8].names}}</span>
        <p class="po1">即将开始</p>
        <p class="po2"><Ds style="font-size: 1.5rem;margin-left: 5rem;"></Ds></p>
      </div>

    </div>
    <div class="repin1">
      <div class="img1"><img style="width: 6.4rem;height: 14.2rem;left: 35%;" :src="arr[9].src" alt="">
        <img style="width: 4rem;height: 7.6rem;" src="/static/img/zi.png" alt="">
        <span style="left: 0;">{{arr[9].names}}</span>
        <p class="po1">即将开始</p>
        <p class="po2"><Ds style="font-size: 1.5rem;margin-left: 5rem;"></Ds></p>
      </div>

      <div class="img1"> <img style="width: 7.7rem;height: 14.3rem;left: 31%;" :src="arr[10].src" alt="">
        <img style="width: 4rem;height: 7.6rem;" src="/static/img/zi.png" alt="">
        <span>{{arr[10].names}}</span>
        <p class="po1">即将开始</p>
        <p class="po2"><Ds style="font-size: 1.5rem;margin-left: 5rem;"></Ds></p>
      </div>

      <div class="img1"><img style="width: 16.9rem;height: 10.4rem;left: 10%;top: 30%;" :src="arr[11].src" alt="">
        <img style="width: 4rem;height: 7.6rem;" src="/static/img/zi.png" alt="">
        <span style="left: 0;">{{arr[11].names}}</span>
        <p class="po1">即将开始</p>
        <p class="po2"><Ds style="font-size: 1.5rem;margin-left: 5rem;"></Ds></p>
      </div>

  </div>
  </div>
</template>

<script>
    import axios from 'axios'
    import Ds from '@/components/Ds'
    export default {
        name: "Kai",
      data(){
        return{
          arr:["/static/img/01.png","/static/img/02.png","/static/img/03.png","/static/img/04.png","/static/img/05.png","/static/img/06.png"],
          img:"/static/img/zi.png",
          arrA:[],
          bol:false
        }
      },
      mounted:function () {
        axios.get('/api/phph0302/zh01.php').then((res)=>{
          this.bol = true;
          this.arr=res.data;
          console.log(this.arr);
        })
      },
      components:{
          Ds
      }
    }
</script>

<style scoped>
  .kaishou{
    text-align: center;
    position: relative;
    margin-top: 3rem;
    background-color: white;
  }
  .ks{
    font-family: MicrosoftYaHei;
    font-size: 3.6rem;
    font-weight: normal;
    font-stretch: normal;
    color: #e53e42;
    margin-top: 2.5rem;
  }
  .mz{
    display: inline-block;
    font-size: 3rem;
    color: #4d4d4d;
    margin-top: 4.3rem;
  }
  .d1,.d2{
    width: 70px;
    height: 2px;background: #cccccc;
  }
  .d1{position: absolute;left: 25rem;top:11.5rem}
  .d2{position: absolute;right: 25rem;top:11.5rem}
  .repin,.repin1{
    width: 65.3rem;
    display: flex;
    position: relative;
    justify-content:space-between ;
    margin-top: 2rem;
    margin-left: 3.5rem;
    background-color: white;
  }
  .repin1{margin-top: 9rem;}
  .img1{border: 1px #cccccc solid;text-align: center;position: relative;
    width: 20rem;height: 24.4rem;}
  .img1 span{font-size: 2.4rem;position: absolute;bottom: 1.5rem;left: 2rem;
    color: #4d4d4d;}
  .img1 img:nth-child(2){position: absolute;left: 0;top: 0;}
  .img1 img:nth-child(1){position: absolute;left: 20%;top: 20%;}
  .djs{position: absolute;left: 0;font-size: 1.8rem;top: 25.5rem;}
  .djs p{
    position: absolute;
    left: 0;
    top: 10rem;
  }
  .repin1{
    padding-bottom: 8rem;
  }
  .repin .po1,.repin1 .po1{
    margin-top: 25rem;
    margin-left: -13rem;
    font-size: 1.8rem;
  }
  .repin .po2,.repin1 .po2{
    margin-left: -14.5rem;
    font-size: 1.8rem;
  }
</style>
