<template>
  <div class="lun">
  <div class="swiper-container">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <router-link to="meishi"><img src="/static/img/dangao.png" alt=""></router-link>
      </div>
      <div class="swiper-slide">
        <router-link to="/lunxiangq"><img src="/static/img/lunbo.png" alt=""></router-link>
      </div>
      <div class="swiper-slide">
        <router-link to="meishi"><img src="/static/img/dangao.png" alt=""></router-link>
      </div>
      <div class="swiper-slide">
        <router-link to="/muying"><img src="/static/img/bibei.png" alt=""></router-link>
      </div>
      <div class="swiper-slide">
        <router-link to="/muying"><img src="/static/img/bibei.png" alt=""></router-link>
      </div>
    </div>

    <div class="swiper-pagination"></div>
  </div>
  </div>
</template>

<script>
    export default {
        name: "Lunbo",
      mounted(){
        var mySwiper = new Swiper('.swiper-container',{
          loop: true,
          autoplay: 2000,
          initialSlide :0,
          speed:500,
          //切换效果
          effect : 'filp',
          pagination : '.swiper-pagination'

        })
      }
    }
</script>

<style scoped>
  .lun{
    width: 100%;
    height: 32.4rem;
  }
  .swiper-container{width: 100%;background:#ffffff;}
  .swiper-slide img{width: 100%;height: 30.4rem;}
</style>
