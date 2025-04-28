<template>
  <swiper
    :cssMode="true"
    :navigation="true"
    :pagination="true"
    :mousewheel="true"
    :keyboard="true"
    :modules="modules"
    class="mySwiper"
  >
    <swiper-slide
      ><img class="w-full h-[50vh]" src="../assets/1.jpg" alt=""
    /></swiper-slide>
    <swiper-slide
      ><img class="w-full h-[50vh]" src="../assets/images.jpeg" alt=""
    /></swiper-slide>
    <swiper-slide
      ><img class="w-full h-[50vh]" src="../assets/images.jpeg" alt=""
    /></swiper-slide>
    <swiper-slide
      ><img class="w-full h-[50vh]" src="../assets/images.jpeg" alt=""
    /></swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/navigation";
import "swiper/css/pagination";

// import required modules
import { Navigation, Pagination, Mousewheel, Keyboard } from "swiper/modules";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation, Pagination, Mousewheel, Keyboard],
    };
  },
};
</script>
<style scoped>

</style>
