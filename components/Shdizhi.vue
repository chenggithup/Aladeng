<template>
  <div class="wrap">
    <div class="toubu"></div>
    <div class="zuo">
      <img src="/static/img/zuo.png" alt="">
    </div>
    <p class="p1">收货地址</p>
    <p class="p2">添加新地址</p>
    <div class="sk1">
      <p class="lisi1">李四</p>
      <p class="tel1">15012340708</p>
      <p class="address1">河南省新乡市红旗区南干道与新中大道交叉口B座10楼102室;</p>
      <p class="youb1">邮编453000</p>
    </div>
    <div class="dj1">
      <div class="bt1">
        <img src="/static/img/hongdian.png" alt="">
      </div>
      <div class="by1">
        <img src="/static/img/dian.png" alt="">
      </div>
      <p class="mr1">默认地址</p>
      <div class="kt1">
        <img src="/static/img/shanchu.png" alt="">
      </div>
      <p class="del1">删除</p>
      <div class="kz1">
        <img src="/static/img/bianji.png" alt="">
      </div>
      <p class="text1">编辑</p>
    </div>
    <div class="sk2">
      <p class="lisi2">李四</p>
      <p class="tel2">15012340708</p>
      <p class="address2">河南省新乡市红旗区南干道与新中大道交叉口B座10楼102室;</p>
      <p class="youb2">邮编453000</p>
    </div>
    <div class="dj2">
      <div class="bt2">
        <img src="/static/img/hui.png" alt="">
      </div>
      <div class="by2">
        <img src="/static/img/huidian.png" alt="">      </div>
      <p class="mr2">默认地址</p>
      <div class="kt2">
        <img src="/static/img/shanchu.png" alt="">
      </div>
      <p class="del2">删除</p>
      <div class="kz2">
        <img src="/static/img/bianji.png" alt="">
      </div>
      <p class="text2">编辑</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Add"
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
    left: 55rem;
    top: 3rem;
  }
  .sk1{
    position: absolute;
    width: 72rem;
    height: 16rem;
    background-color: white;
    top: 10rem;
  }
  .lisi1{
    position: absolute;
    font-size:2.8rem;
    left: 2rem;
    top: 1rem;
  }
  .tel1{
    position: absolute;
    font-size: 2.8rem;
    top: 1rem;
    left: 18rem;
  }
  .address1{
    position: absolute;
    font-size: 2.4rem;
    top: 8rem;
    left: 2rem;
    color: #666666;
  }
  .youb1{
    position: absolute;
    font-size: 2.4rem;
    top: 12rem;
    left: 2rem;
    color: #666666;
  }
  .dj1{
    position: absolute;
    width: 72rem;
    height: 8rem;
    background-color: white;
    top: 26.3rem;
  }
  .bt1 img{
    position: absolute;
    width:3rem;
    height: 3rem;
    left: 2rem;
    top: 2.5rem;
  }
  .by1 img{
    position: absolute;
    width: 1rem;
    height: 1rem;
    top: 3.5rem;
    left: 3rem;
  }
  .mr1{
    position: absolute;
    font-size: 2.4rem;
    top: 2.5rem;
    left: 7rem;
  }
  .kt1 img{
    position: absolute;
    width:3rem;
    height: 3rem;
    top: 2rem;
    left: 61rem;
  }
  .del1{
    position: absolute;
    font-size: 2.4rem;
    left: 65rem;
    top: 2rem;
  }
  .kz1 img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    top: 2rem;
    left: 49rem;

  }
  .text1{
    position: absolute;
    font-size: 2.4rem;
    top: 2rem;
    left: 53rem;
  }
  .sk2{
    position: absolute;
    width: 72rem;
    height: 16rem;
    background-color: white;
    top: 34.6rem;
  }
  .lisi2{
    position: absolute;
    font-size:2.8rem;
    left: 2rem;
    top: 1rem;
  }
  .tel2{
    position: absolute;
    font-size: 2.8rem;
    top: 1rem;
    left: 18rem;
  }
  .address2{
    position: absolute;
    font-size: 2.4rem;
    top: 8rem;
    left: 2rem;
    color: #666666;
  }
  .youb2{
    position: absolute;
    font-size: 2.4rem;
    top: 12rem;
    left: 2rem;
    color: #666666;
  }
  .dj2{
    position: absolute;
    width: 72rem;
    height: 8rem;
    background-color: white;
    top: 50.7rem;
  }
  .bt2 img{
    position: absolute;
    width:3rem;
    height: 3rem;
    left: 2rem;
    top: 2.5rem;
  }
  .by2 img{
    position: absolute;
    width: 1rem;
    height: 1rem;
    top: 3.5rem;
    left: 3rem;
  }
  .mr2{
    position: absolute;
    font-size: 2.4rem;
    top: 2.5rem;
    left: 7rem;
  }
  .kt2 img{
    position: absolute;
    width:3rem;
    height: 3rem;
    top: 2rem;
    left: 61rem;
  }
  .del2{
    position: absolute;
    font-size: 2.4rem;
    left: 65rem;
    top: 2rem;
  }
  .kz2 img{
    position: absolute;
    width: 3rem;
    height: 3rem;
    top: 2rem;
    left: 49rem;

  }
  .text2{
    position: absolute;
    font-size: 2.4rem;
    top: 2rem;
    left: 53rem;
  }
</style>
