<template>
  <div class="wrap">

    <div class="one">
      <div v-for="(item,index) in arr" class="hufu">
        <img class="hufu02" src="/static/img/06.png" alt="">
        <div class="ms">
          <span>面部美白爽</span><br>
          <span class="zhi">¥13.5</span>
          <button class="xian">立即购买</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Lxqtwo",
    data(){
      return{
        arr:[1,2,3,4]
      }
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
    background-color: ;
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
    width: 17rem;
    height: 10rem;
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
