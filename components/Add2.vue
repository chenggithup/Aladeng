<template>
    <div class="wrap">
      <div class="toubu"></div>
      <div class="zuo">
        <router-link to="/address"><img src="/static/img/zuo.png" alt=""></router-link>
      </div>
      <p class="p1">添加新地址</p>
      <p class="p2" @click="fs()">完成</p>
      <p class="nn">请使用您的真实姓名，否则订单将无法发出</p>
      <div class="nam">
        <input  class="inp" type="text" placeholder="请填写真实姓名">
      </div>
      <div class="phone">
        <input type="text" class="tel" placeholder="请填写手机号">
      </div>
        <div class="city">

          <span class="sheng">请选择城市</span>
          <span class="shi"></span>
          <span class="qu"></span>
          <img @click="choose" src="/static/img/you.png" alt="">
          <div class="divwrap" v-if="show">
            <v-distpicker type="mobile" @province="onChangeProvince" @city="onChangeCity" @area="onChangeArea"></v-distpicker>
          </div>
        </div>
      <div class="ad">
        <input type="text" class="dizhi" placeholder="请填写详细地址">
      </div>
      <div class="yb">
        <input type="text" class="zip" placeholder="请填写邮编">
      </div>
    </div>

</template>
<script>
  import axios from 'axios'
  import VDistpicker from 'v-distpicker'
    export default {
        name: "Add2",
      data(){
        return{
          show:false
        }
      },
      components: { VDistpicker },
        methods:{
          fs(){
            alert('保存成功!');
            this.$router.push('/add');
            var mingzi = $('.inp').val();
            var sjh = $('.tel').val();
            var dz = $('.dizhi').val();
            var zip = $('.zip').val();
            var city1 = $('.sheng').html();
            var city2 = $('.shi').html();
            var city3 = $('.qu').html();
            var params = new URLSearchParams();
            params.append('name',mingzi);
            params.append('tel',sjh);
            params.append('dizhi',dz);
            params.append('zip',zip);
            params.append('city',city1);
            params.append('shi',city2);
            params.append('qu',city3);
            axios.post('/api/phph0302/address.php',params).then(function(res){
              console.log(res.data);
            }.bind(this));

          },
          choose(){
            this.show=!this.show
          },
          onChangeProvince(a){
            console.log(a.value);
            $('.sheng').html(a.value);
          },
          onChangeCity(a){
//            console.log(a)
            $('.shi').html(a.value);
          },
          onChangeArea(a){
//            console.log(a)
            $('.qu').html(a.value);
            this.show=false
          }
        }
    }

</script>

<style scoped>
  .wrap{
    margin: 0;
    padding: 0;
    width:72rem;
    height: 128rem;
    background-color:rgb(242,242,242) ;
    position: relative;
  }
  .toubu{
    position: absolute;
    border: 1px solid rgb(229,62,66);
    width: 72rem;
    height: 9.6rem;
    background-color: rgb(229,62,66);
  }
  .zuo img{
    position: absolute;
    left:3rem;
    top: 3rem;
    width: 2.3rem;
    height: 3.8rem;
  }
  .p1{
    position: absolute;
    font-size: 3.6rem;
    color: white;
    left: 28rem;
    top: 3rem;
  }
  .p2{
    position: absolute;
    font-size: 3rem;
    color: white;
    left: 62rem;
    top: 3.5rem;
  }
  .nn{
   position: absolute;
    font-size: 2.4rem;
    color:rgb(229,62,66);
    top: 12rem;
    left: 2rem;
  }
  .nam input{
    position: absolute;
    width: 72rem;
    font-size: 2.8rem;
    height: 10rem;
    background-color: rgb(255,255,255);
    top: 17rem;
    border: 1px solid rgb(204,204,204);
    left: -0.1rem;
  }
  .phone input{
    position: absolute;
    width: 72rem;
    font-size: 2.8rem;
    height: 10rem;
    background-color: rgb(255,255,255);
    top: 29rem;
    border: 1px solid rgb(204,204,204);
    left: -0.1rem;
  }
   .city{
     position: absolute;
     width: 72rem;
     height: 10rem;
     background-color: rgb(255,255,255);
     top: 39.2rem;
   }
  .city p{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(128,128,128);
    top: 2.5rem;
  }
  .city img{
    position: absolute;
    width: 1rem;
    height:1.8rem;
    top: 3.5rem;
    left: 70rem;
  }
  .ad input{
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color:rgb(255,255,255);
    top: 49.4rem;
    border: 1px solid rgb(204,204,204);
    left: -0.1rem;
    font-size: 2.8rem;
  }
  .yb input {
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color:rgb(255,255,255);
    border: 1px solid rgb(204,204,204);
    top: 59.6rem;
    font-size: 2.8rem;
    left: -0.1rem;
  }


  .divwrap{
    height: 400px;
    overflow-y: auto;
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
  }
  .divwrap>>>.distpicker-address-wrapper{
    color: #999;
    font-size: 3rem;
  }
  .divwrap>>>.address-header{
    position: fixed;
    bottom: 400px;
    width: 100%;
    background: #000;
    color:#fff;
    font-size: 3rem;
  }
  .divwrap>>>.address-header ul li{
    flex-grow: 1;
    text-align: center;
  }
  .divwrap>>>.address-header .active{
    color: #fff;
    border-bottom:#666 solid 8px
  }
  .divwrap>>>.address-container .active{
    color: #000;
  }
.sheng,.shi,.qu{
  font-size: 2.8rem;
  position: absolute;
  color: #808080;
}
.sheng{
  left: 0;
  top: 2.2rem;
}
  .shi{
    left: 14rem;
    top: 2.2rem;
  }
  .qu{
    left: 35rem;
    top: 2.2rem;
  }
</style>
