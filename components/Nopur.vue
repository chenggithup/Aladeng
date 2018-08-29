<template>
    <div class="wrap">
      <div class="hd">
        <p>购物车</p>
      </div>
      <div class="mi"></div>
      <p class="pp">您的购物车还是空的</p>
      <p class="pp1">去<a href="http://localhost:8080/#/shouye">逛逛</a>吧</p>
      <div class="bottom">
        <div>
          <router-link to="/shouye"><img style="width:4.8rem;height: 4.8rem;" src="/static/img/shouyeqian.png" alt=""></router-link>
          <p>首页</p>
        </div>
        <div>
          <router-link to="/fenlei"><img style="width:4.8rem;height: 4.8rem;" src="/static/img/fenleiqian.png" alt=""></router-link>
          <p>分类</p>
        </div>
        <router-link to="/dhuowang"><div>
          <img style="width:11.3rem;height: 5.5rem;" src="/static/img/duanhuo.png" alt="">
        </div></router-link>
        <router-link to="/nopur"><div>
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
    export default {
        name: "Nopur",
        data(){
          return{
            n:0
          }
        },
        methods:{
      mm(){
        this.n++;
        if(this.n % 2 ==0){
          document.getElementsByClassName("m2")[0].src="/static/img/gouwuche.png";
          document.getElementsByClassName("pp2")[0].style.color= '';
        }else{
          document.getElementsByClassName("m2")[0].src="/static/img/gouwuchehou.png";
          document.getElementsByClassName("pp2")[0].style.color= '#f00';
        }
      }
        }

    }
</script>

<style scoped>
   .wrap{
     width: 100%;
   }
   .hd{
     margin-top: 8rem;
     width: 100%;
     text-align: center;
     height: 9rem;
     line-height: 9rem;
     background-color: #f00;
   }
  .hd p{
    font-size: 3.6rem;
    color: #ffffff;
  }
  .mi{
    margin-top: 11.6rem;
    width: 32.5rem;
    height: 26.1rem;
    margin-left: 20rem;
    background-color: #efc5c5;
  }
   .bottom{
     border-top: 1px solid #e6e6e6;
     margin-top: 10rem;
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
   }
   .bottom img{
     margin-top: 1.5rem;
   }
   .pp{
     margin-top: 3rem;
     font-size: 2.4rem;
   }
   .pp1{
     margin-top: 1rem;
     margin-left: -12rem;
     font-size: 2.4rem;
   }
   .pp1 a{
     text-decoration: none;
     color: #ea6568;
   }
   p{
     margin-top: -8rem;
     font-size: 2rem;
   }
</style>
