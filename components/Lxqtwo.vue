<template>
  <div v-if="bol" class="wrap">

    <div class="one">
      <div v-for="(item,index) in arr" class="hufu">
        <img class="hufu02" :src="arrA[14].src" alt="">
        <div class="ms">
          <span>{{arrA[14].names}}</span><br>
          <span class="zhi">{{arrA[14].jiage}}</span>
          <button class="xian">立即购买</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import axios from 'axios'
  export default {
    name: "Lxqtwo",
    data(){
      return{
        arr:[1,2,3,4],
        bol:false,
        arrA:[]
      }
    },
    mounted: function () {
      axios.get("/api/phph0302/zh01.php").then((res)=>{
        this.arrA=res.data;
        console.log(this.arrA);
        this.bol=true;
      })
    }
  }
</script>

<style scoped>
  *{margin: 0;padding: 0;}
  .wrap{ background-color: #feeaf5;}
  .one{
    width: 100%;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
  }
  .hufu{
    width: 33rem;
    height: 41rem;
    border: 1px #cccccc solid;
    text-align: center;
    background-color: white;
    margin-top: 1rem;
  }
  .hufu02{
    width: 13rem;
    height: 12rem;
    margin-top: 6.4rem;
  }
  .ms{
    border-top: 1px #cccccc solid;
    margin-top: 10rem;
    font-size: 2.4rem;
    position: relative;
  }
  .ms img{
    width: 2.4rem;
    height: 1.6rem;
  }
  .zhi{
    color: red;
  }
  .xian{
    position: absolute;
    width: 21.8rem;
    height: 3rem;
    background-color: red;
    border-radius: 1.5rem;
    text-align: center;
    left: 5rem;
    bottom: -3rem;
    color: white;
  }

</style>
