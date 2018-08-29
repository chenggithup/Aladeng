<template>
    <div v-if="bol" class="wrap">
      <div class="top">
        <router-link to="/geren"><img src="/static/img/fanhui.png" alt=""></router-link>
        <span class="shouhuo">收获地址</span>
        <span @click="add2()" class="add">添加新地址</span>
      </div>
       <ul v-for="(item,index) in arr" class="ul1">
         <li class="li1">
           <span class="name">{{arr[index].name}}</span>
           <span class="tel">{{arr[index].tel}}</span><br>
           <span class="dizhi">{{arr[index].dizhi}}</span>
           <span style="top: 12rem;" class="dizhi">邮编:{{arr[index].zip}}</span>
         </li>
         <li class="li2">
           <img class="hd" src="/static/img/hongdian.png" alt="">
           <span class="moren">默认地址</span>
           <img class="bj" src="/static/img/bianji.png" alt="">
            <span class="bianji">编辑</span>
           <img class="data" src="/static/img/shanchu.png" alt="">
           <span @mouseover="del()" class="shanchu">删除</span>
         </li>
       </ul>


    </div>
</template>

<script>
  import axios from 'axios'

    export default {
        name: "Add",
      data(){
        return {
          bol:false,
          arr:[]

        }
      },

      methods:{
     del(){
       $('.shanchu').click(function(){
         $(this).parent().parent().remove();
       });
     },
        add2(){
          this.$router.push('/add2');
        },

      },
      mounted:function (){
        axios.get('/api/phph0302/vueb.php').then((res)=>{
        this.arr = res.data;
        console.log(res.data);
        this.bol = true;
      });

      }
    }
</script>

<style scoped>
*{margin: 0;padding: 0;}
.wrap{
  background-color: #cccccc;
  width: 100%;
  height: 100%;
}
.top{display: flex;justify-content:space-between;background-color: red;
  height: 11.3rem;
  width: 100%;
 position: relative;
}
.top img{
  width: 2.3rem;
  height: 3.8rem;
  margin-top:3.7rem;
  margin-left: 2rem;
}
.add{
  font-size: 3rem;
  margin-top: 3.7rem;color: white;

}
.shouhuo{font-size: 3.6rem;margin-top: 3.7rem;color: white;
position: absolute;
  left: 28.7rem;
}
.ul1{
  width: 100%;
  height: 24rem;
  background-color: #ffffff;
  text-align: left;
}
.li1{
  width: 100%;
  height: 16rem;
  border-bottom: 1px #cccccc solid;
  position: relative;
}
 .name{
   position: absolute;
   top: 3rem;
   font-size: 2.8rem;
   left: 5rem;
   color: #4d4d4d;
 }
.tel{
  position: absolute;
  top: 3rem;
  font-size: 2.8rem;
  left: 18rem;
  color: #4d4d4d;
}
  .dizhi{
    position: absolute;
    font-size: 2.4rem;
    color: #808080;
    left: 5rem;
    top:8rem;
    width: 66.5rem;
    height: 5.9rem;
  }
  .li2{
    width: 100%;
    height: 8rem;
    line-height: 8rem;
    position: relative;
    border-bottom: 1px #cccccc solid;
  }
  .li2 img{
    width: 3rem;
    height: 3rem;
    position: absolute;
  }
  .li2 span{
    font-size: 2.4rem;
    position: absolute;
  }

  .hd{
    left: 3rem;
    top: 3.5rem;
  }
.moren{
  left: 7rem;
  top: 1.1rem;
}
 .bj{
   right: 23rem;
   top:2.9rem;
 }
  .bianji{
    right: 17rem;
    top:0.9rem;
  }
.data{
  right: 9rem;
  top: 2.9rem;
}
  .shanchu{
    right: 3rem;
    top: 0.9rem;
  }
</style>
