<template>
  <div class="wrap">
    <div class="toubu"></div>
    <div class="zuo">
      <router-link to="/grxx"><img src="/static/img/zuo.png" alt=""></router-link>
    </div>
    <p class="p1">修改手机号</p>
    <p class="p2" @click="save()">保存</p>
    <div class="sw">
      <input type="text" value="" placeholder="请输入新手机号">
    </div>
  </div>
</template>

<script>
  export default {
    name: "Phone",
    methods:{
      save(){
        alert("修改成功");
        $("input").val('');
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

  }
  .toubu{
    position: relative;
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
  .sw{
    width: 100%;
    height: 8rem;
    line-height: 8rem;
    border-bottom: 2px solid #ccc;
    position: relative;
    background-color: #fff;
  }
  .sw input{
    position: absolute;
    width: 68rem;
    height: 8rem;
    top: 0rem;
    left: 2rem;
    font-size: 2.8rem;
  }
  input::-webkit-input-placeholder {
    font-size: 2.8rem;
    text-align: left;
  }
</style>
