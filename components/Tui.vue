<template>
    <div v-if="bol" class="tui">
      <router-link to="/yan"><div class="shang"><img src="/static/img/xuanli.png" alt=""></div></router-link>
      <div class="xia xia1">
        <div class="lf">
          <router-link to="/koured"><img :src="arr[0].src" alt=""></router-link>
          <p class="p1">{{arr[0].names}}</p>
          <p class="p2">{{arr[0].jiage}}</p>
        </div>
        <div class="shu"></div>
        <div class="center">
          <router-link to="/spin"><img :src="arr[1].src" alt=""></router-link>
          <p class="p1">{{arr[1].names}}</p>
          <p class="p2">{{arr[1].jiage}}</p>
        </div>
        <div class="shu"></div>
        <div class="rt">
          <router-link to="/xiangqing"><img :src="arr[2].src" alt=""></router-link>
          <p class="p1">{{arr[2].names}}</p>
          <p class="p2">{{arr[2].jiage}}</p>
        </div>
      </div>
    </div>
</template>

<script>
    import axios from 'axios'
    export default {
        name: "Tui",
        data(){
          return{
            arr:[],
            bol:false
          }
        },
        mounted: function () {
          axios.get("/api/phph0302/zh01.php").then((res)=>{
            this.arr=res.data;
            console.log(this.arr);
            this.bol=true;
          })
        }
    }
</script>

<style scoped>
  .tui{
    height: 60rem;
  }
  .shang img{
    width: 100%;
    vertical-align: bottom;
  }
  .xia{
    display: flex;
    justify-content: center;
    background-color: #fff;
    padding-top: 1rem;
  }
  .xia img{
    width: 6.9rem;
    height: 15.3rem;
  }
  .lf,.center{
    padding-right: 6rem;
  }
  .center,.rt{
    padding-left: 6rem;
  }
  .shu{
    width: 0.1rem;
    height: 18rem;
    background-color: #cccccc;
  }
  .p1{
    font-size: 2.4rem;
    margin-top: 2rem;
  }
  .p2{
    font-size: 2.4rem;
    color: #e83d41;
    margin-top: 1rem;
  }
</style>
