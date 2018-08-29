<template>
  <div class="wrap">

    <div class="one">
      <div v-for="(item,index) in arr" class="hufu">
        <img class="hufu02" src="/static/img/naifein.png" alt="">
        <div class="ms">
          <span>三鹿奶粉</span><br>
          <span class="zhi">9.9</span> <img src="/static/img/niaohu.png" alt="">
          <div class="xian"></div> <p class="jiage">¥99.9</p>
        </div>
      </div>



    </div>
  </div>
</template>

<script>
  export default {
    name: "Two",
    data(){
      return{
        arr:[1,2,3,4]
      }
    }
  }
</script>

<style scoped>
  *{margin: 0;padding: 0;}
  .wrap{background-color: white;}
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

  }
  .hufu02{
    width: 14.3rem;
    height: 14.3rem;
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
    width: 7rem;
    height: 0.2rem;
    background-color: #808080;
    left: 13rem;
    bottom: 1.2rem;
  }
  .jiage{
    font-size: 2.2rem;
    color: #808080;
  }
</style>
