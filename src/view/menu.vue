<template>
    <div class="content w-full bg-black" id="menu">
        <swiper
      :slides-per-view="3"
      :space-between="50"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
    >
      <swiper-slide><img src="../img/shop1.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="../img/shop2.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="../img/shop3.jpg" alt=""></swiper-slide>
      ...
    </swiper>
    </div>
  </template>
  <script>
    // Import Swiper Vue.js components
    import { Swiper, SwiperSlide } from 'swiper/vue';
  
    // Import Swiper styles
    import 'swiper/css';
  
    export default {
      components: {
        Swiper,
        SwiperSlide,
      },
      setup() {
        const onSwiper = (swiper) => {
          console.log(swiper);
        };
        const onSlideChange = () => {
          console.log('slide change');
        };
        return {
          onSwiper,
          onSlideChange,
        };
      },
    };
  </script>
  <style>
.content{
    height: 50vh;
}
</style>