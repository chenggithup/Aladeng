<template>
  <div class="lun">
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          <img src="/static/img/chuncai.png" alt="">
        </div>
        <div class="swiper-slide">
          <img src="/static/img/chuncai.png" alt="">
        </div>
        <div class="swiper-slide">
          <img src="/static/img/chuncai.png" alt="">
        </div>
        <div class="swiper-slide">
          <img src="/static/img/chuncai.png" alt="">
        </div>
        <div class="swiper-slide">
          <img src="/static/img/chuncai.png" alt="">
        </div>
      </div>

      <div class="swiper-pagination"></div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Lunbo03",
    mounted(){
      var mySwiper = new Swiper('.swiper-container',{
        loop: true,
        autoplay: 1000,
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
  .swiper-container{width: 100%;background:#ffffff;
    height: 36rem;}
  .swiper-slide{text-align: center;}
  .swiper-slide img{width: 12rem;height: 24.5rem;margin-top: 3rem;}

</style>
