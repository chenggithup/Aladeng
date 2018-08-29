<template>
    <div class="fi fi1">
      <div class="bo">
        <div class="peisong">
          <span>订单编号:485269676465</span>
          <span>待发货</span>
        </div>
        <ul class="ul1">
          <li class="li2">
            <div class="shangp">
              <img src="/static/img/01.png" alt="">
              <span class="sp1">会呼吸丝滑蜜粉</span>
              <span class="sp2">规格 : 蜜粉</span>
              <p><span class="sp3">¥166.06</span> ✖️1件</p>

            </div>

          </li>
        </ul>
        <Daojishi></Daojishi>
      </div>

    </div>
</template>

<script>
    import Daojishi from '@/components/Daojishi'
    export default {
        name: "First",
      components:{
          Daojishi
      }
    }
</script>

<style scoped>
  .peisong{
    height: 6rem;
    line-height: 6rem;
    background-color: #fff;
    border-bottom: 1px solid #ccc;
  }
  .peisong span:first-child{
    font-size: 2.8rem;
    float: left;
    margin-left: 2rem;
  }
  .peisong span:last-child{
    font-size: 2.8rem;
    float: right;
    margin-right: 2rem;
    color: #f00;
  }
  .ul1{
    list-style-type: none;
    background-color: #fff;
  }
  .li2{
    position: relative;
    width: 100%;
    height: 20rem;
    border-bottom:1px #cccccc solid;
  }
  .shangp{
    position: absolute;
    left: 10rem;
    top:5rem;
    width: 32.9rem;
    height: 14.1rem;
  }
  .shangp img{
    width: 8.6rem;
    height: 10rem;
    position: absolute;
    left: 1rem;
  }
  .sp1{
    width: 20rem;
    position: absolute;
    top: 0rem;
    left: 15rem;
    font-size: 2.8rem;
    color: #4d4d4d;
  }
  .sp2{
    position: absolute;
    top: 5rem;
    left: 15rem;
    font-size: 2.4rem;
    color: #666666;
  }
  .shangp p{
    position: absolute;
    left: 25rem;
    top: 10rem;
    font-size: 2.8rem;
    color: #808080;
  }
  .sp3{
    position: absolute;
    left: -10rem;
    top: 0;
    font-size: 2.4rem;
    color: red;
  }
</style>
