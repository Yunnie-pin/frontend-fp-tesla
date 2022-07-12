<template>
    <swiper :pagination="true" :modules="modules" :loop="true" class="mySwiper"     :autoplay="{delay: 2500,disableOnInteraction: false,}" >
            <swiper-slide>
                <img src="dist/image/cars/slider/crop-M3-Homepage-Desktop-LHD.jpg" alt="Model 3" class="w-full">
                </swiper-slide>
            <swiper-slide>
                <img src="dist/image/cars/slider/crop-Desktop-ModelY.jpg" alt="Model Y" class="w-full">
            </swiper-slide>
            <swiper-slide>
                <img src="dist/image/cars/slider/crop-Homepage-Model-S-Desktop-LHD.jpg" alt="Model S" class="w-full">
            </swiper-slide>
            <swiper-slide>
                <img src="dist/image/cars/slider/crop-Homepage-Model-X-Desktop-LHD.jpg" alt="Model X" class="w-full">
            </swiper-slide>
    </swiper>

</template>

<script>

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

// import required modules
import { Autoplay, Pagination } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
        modules: [Autoplay,Pagination],

    };
  },
};
</script>

<style></style>