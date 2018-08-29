<template>
<div v-if="bol" id="wrap">
  <div class="naifen">
    <img src="/static/img/woniu.png" alt="">

  <div class="naifen2">
    <span class="ms">{{arr[9].names}}</span><br>
    <span class="jg">{{arr[9].jiage}}</span><br>
    <router-link to="/gouwu"><button>立即购买</button></router-link>
  </div>
  </div>
  <div class="naifen">
    <img src="/static/img/woniu.png" alt="">

  <div class="naifen2">
    <span class="ms">{{arr[9].names}}</span><br>
    <span class="jg">{{arr[9].jiage}}</span><br>
    <router-link to="/gouwu"><button>立即购买</button></router-link>
  </div>
  </div>

  <div class="naifen">
    <img src="/static/img/woniu.png" alt="">

    <div class="naifen2">
      <span class="ms">{{arr[9].names}}</span><br>
      <span class="jg">{{arr[9].jiage}}</span><br>
      <router-link to="/gouwu"><button>立即购买</button></router-link>
    </div>
  </div>

  <div class="naifen">
    <img src="/static/img/woniu.png" alt="">

    <div class="naifen2">
      <span class="ms">{{arr[9].names}}</span><br>
      <span class="jg">{{arr[9].jiage}}</span><br>
      <router-link to="/gouwu"><button>立即购买</button></router-link>
    </div>
  </div>

</div>
</template>

<script>
    import axios from 'axios'
    export default {
        name: "Naifen",
      data(){
        return{
          bol:false,
          arr:[]
        }
      },
      mounted: function () {
        axios.get('/api/phph0302/zh01.php').then((res)=>{
          this.bol=true;
          this.arr=res.data;
        })
      }
    }
</script>

<style scoped>
*{margin: 0;padding: 0;}
  #wrap{
    width: 100%;background-color: #f2f2f2; display: flex;
    justify-content: space-around;flex-flow: wrap;}
  .naifen{
    width: 33rem;
    height: 44rem;
    border: 1px #cccccc solid;
    background-color: white;
    text-align: center;
     margin-top: 2rem;
  }
  .naifen img{
    width: 6.4rem;
    height: 15.2rem;
    margin-top: 4rem;
  }
  .naifen2{
    border-top: 1px #cccccc solid;
    height: 17.6rem;
    margin-top: 6rem;
  }
  .naifen2 span{
    font-size: 2.4rem;

  }
  .naifen2 button{
  width: 21.8rem;
  height: 3rem;
  background-color: #e53e42;
  border-radius: 1.5rem;
  text-align: center;
    line-height: 3rem;
    font-size: 1.8rem;
    color: white;

  }
  .jg{
    color: red;
    font-size: 1.8rem;
    display: block;
    margin-top: 2rem;
  }
  .ms{
    color: #4d4d4d;
    display: block;
    margin-top: 2rem;
  }

</style>
