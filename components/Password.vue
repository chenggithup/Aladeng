<template>
    <div class="wrap">
      <div class="toubu"></div>
      <div class="zuo">
        <router-link to="qingchu"><img src="/static/img/zuo.png" alt=""></router-link>
      </div>
      <p class="p1">设置</p>
      <p class="p2" @click="com()">完成</p>
      <div class="password">
        <div class="pw">
          输入原密码:<input type="text" placeholder="请输入原密码" value="">
        </div>
      </div>
      <div class="password1">
        <div class="pw1">
          输入新密码:<input type="text" placeholder="请输入新密码" value="">
        </div>
    </div>
      <div class="password2">
        <div class="pw2">
          确认新密码:<input type="text" placeholder="请确认新密码" value="">
        </div>
      </div>
      s</div>
</template>

<script>
    export default {
        name: "Password",
        methods:{
          com(){
            alert("修改成功");
            $(".pw input").val('');
            $(".pw1 input").val('');
            $(".pw2 input").val('');
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
    left: 64rem;
    top: 3rem;
  }
  .password{
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color: white;
    top:10rem;
  }
  .pw{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    top: 3rem;
    left: 2rem;
  }
  .sw{
    position: absolute;
    font-size: 2.4rem;
    color:rgb(128,128,128);
    top: 3.5rem;
    left: 20rem;
  }
  .password1{
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color: white;
    top:20.2rem;
  }
  .pw1{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    top: 3rem;
    left: 2rem;
  }
  .sw1{
    position: absolute;
    font-size: 2.4rem;
    color:rgb(128,128,128);
    top: 3.5rem;
    left: 20rem;
  }
  .password2{
    position: absolute;
    width: 72rem;
    height: 10rem;
    background-color: white;
    top:30.5rem;
  }
  .pw2{
    position: absolute;
    font-size: 2.8rem;
    color: rgb(77,77,77);
    top: 3rem;
    left: 2rem;
  }
  .sw2{
    position: absolute;
    font-size: 2.4rem;
    color:rgb(128,128,128);
    top: 3.5rem;
    left: 20rem;
  }
</style>
