<template>
<div class="wrap">
  <div class="top">
    <span>注册</span>
  </div>

<div v-show="bol" class="tishi">
  <span>验证码已发送至您的手机请注意查收</span>
</div>


  <div class="inp1">
    <img src="/static/img/shouji.png" alt="">
     <div class="xian"></div>
    <div @click="cha()" class="cha">x</div>
    <input type="text" class="phone" placeholder="请输入手机号">
  </div>

  <div class="inp2">
    <img src="/static/img/yanz.png" alt="">
    <div class="xian"></div>
    <input type="text" value="" class="yanz01" placeholder="输入手机验证码">
    <button @click="abc()" class="yanz">获取验证码</button>
  </div>

  <div class="inp1">
    <img src="/static/img/yaoq.png" alt="">
    <div class="xian"></div>
    <input type="text" value="" placeholder="请输入邀请码">
  </div>

  <div class="btn">
    <button class="qux">取消</button>
    <button class="wanc">完成</button>
  </div>

</div>
</template>

<script>
    export default {
        name: "Zhuce",
        data(){
          return{
      bol:false
          }
        },
      methods:{
       abc() {
         var _this = this;
         var a= 60+'秒';
      var myreg = /^(((13[0-9]{1})|(15[0-9]{1})|(18[0-9]{1}))+\d{8})$/;
      if(!myreg.test($(".phone").val()))
      {
        alert('请输入有效的手机号码！');
        return false;
      }else {
          _this.bol = true;
          $(".yanz").html(a);
         clearInterval(time);
          var time = setInterval(function(){
            a-=1;
            $(".yanz").html(a+"秒");
            if (a==0){
              $(".yanz").html('重新获取');
              clearInterval(time);
            }
          },1000);
          setTimeout(function () {
            var aa = Math.floor(Math.random()*(999999-0)+0);
            $(".yanz01").val(aa);
          },10000);

      }
    },
        cha(){
          $(".cha").click(function () {
            $("#phone").val('');
          });
        }
      },
      mounted:function () {

      }
    }
</script>

<style scoped>
*{margin: 0;padding: 0;}
 .wrap{background-color: #f2f2f2;
   width: 100%;
   height: 128rem;
 }
  .top{
    width: 100%;
    height: 9.6rem;
    background-color: red;
  }
  .top span{
    font-size: 3.6rem;
    color: white;
    line-height: 9.6rem;
  }
  .inp1{
  width: 60rem;
  height: 6rem;
  background-color: #ffffff;
  border-radius: 3rem;
    margin-top: 5rem;
    margin-left: 6rem;
  border: solid 1px #cccccc;
    position: relative;
}
.inp2{
  width: 38rem;
  height: 6rem;
  background-color: #ffffff;
  border-radius: 3rem;
  margin-top: 5rem;
  margin-left: 6rem;
  border: solid 1px #cccccc;
  position: relative;
}
.inp1 img,.inp2 img{
  width: 2.2rem;
  height: 3rem;
  position: absolute;
  left: 6rem;
  top:1.5rem;
}
  .xian{
    width: 0.2rem;
    height: 4rem;
    background-color: #cccccc;
    position: absolute;
    left: 10rem;
    top: 1rem;
  }
  .cha{
    width: 2.4rem;
    height: 2.4rem;
    border: 1px #808080 solid;
    color: #808080;
    text-align: center;
    position: absolute;
    right: 2rem;
    font-size: 2.8rem;
    line-height: 2rem;
    top:1.5rem;
    border-radius: 50%;
  }
  .inp1 input,.inp2 input{
    text-align: center;
    font-size: 2.3rem;
    line-height: 6rem;
  }
.yanz {
  width: 20rem;
  height: 6rem;
  background-color: #ffffff;
  border-radius: 3rem;
  border: solid 1px #4d4d4d;
  position: absolute;
  right: -23rem;
  font-size: 2.4rem;
  color: black;
}
  .btn{
    width: 68rem;
    height: 8rem;
    line-height: 8rem;
    margin-left: 2rem;
    margin-top: 5rem;
    font-size: 2.8rem;

  }
  .qux{
    width: 24rem;
    height: 6rem;
    background-color: #ffffff;
    border-radius: 3rem;
    border: 1px #4d4d4d solid;
  }
  .wanc{
    width: 24rem;
    height: 6rem;
    background-color: red;
    border-radius: 3rem;
    margin-left: 10rem;
    color: white;
  }
.tishi span{
  font-size: 2.8rem;
  color: red;
}
</style>
