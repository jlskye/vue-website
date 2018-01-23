<template>

      <!-- swiper -->
      <div class="swiper-movie">
      <swiper :options="swiperOption">
        <swiper-slide class="pic1"></swiper-slide>
        <swiper-slide class="pic2"></swiper-slide>
        <swiper-slide class="pic3"></swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
      </div>
</template>

<script>

import { swiper, swiperSlide } from 'vue-awesome-swiper'
require('swiper/dist/css/swiper.css')
  export default {
   components: {
            swiper,
            swiperSlide
        },
    data() {
      return {
        swiperOption: {
          effect: 'coverflow',
          grabCursor: true,
          centeredSlides: true,
          slidesPerView: 'auto',
          coverflowEffect: {
            rotate: 50,
            stretch: 0,
            depth: 100,
            modifier: 1,
            slideShadows : true
          },
          pagination: {
            el: '.swiper-pagination'
          }
        }
      }
    }
  }
</script>

<style lang="css">
  .swiper-slide {
    background: center ;
    background-size: cover;
    width: 300px;
    height: 300px;
    margin-top: 50px;
    border: 2px solid #000000
  }
  .swiper-movie{
  width:80%;
  margin-left:100px;
  margin-top:80px;

  background:yellow ;
  }
  .pic1{
  background-image:url(../assets/pic1.jpg);
  }
 .pic2{
  background-image:url(../assets/pic2.jpg);
  }
 .pic3{
  background-image:url(../assets/pic3.jpg);
  }
</style>

