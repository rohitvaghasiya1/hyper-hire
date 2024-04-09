<template>
  <swiper
    :slidesPerView="3"
    :spaceBetween="20"
    class="mySwiper"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    :loop="true"
    :modules="modules"
  >
    <swiper-slide>
      <div class="flex items-center bottom-slider">
        <div><img src="../assets/img-1.png" alt="Slider" /></div>
        <div>
          <h3 class="slider-title q-pl-lg fw-900 q-my-none">해외 마케팅</h3>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="flex items-center bottom-slider">
        <div><img src="../assets/img-2.png" alt="Slider" /></div>
        <div>
          <h3 class="slider-title q-pl-lg fw-900 q-my-none">퍼블리셔</h3>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="flex items-center bottom-slider">
        <div><img src="../assets/img-3.png" alt="Slider" /></div>
        <div>
          <h3 class="slider-title q-pl-lg fw-900 q-my-none">캐드원(제도사)</h3>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="flex items-center bottom-slider">
        <div><img src="../assets/img-4.png" alt="Slider" /></div>
        <div>
          <h3 class="slider-title q-pl-lg fw-900 q-my-none">해외 세일즈</h3>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="flex items-center bottom-slider">
        <div><img src="../assets/img-1.png" alt="Slider" /></div>
        <div>
          <h3 class="slider-title q-pl-lg fw-900 q-my-none">해외 마케팅</h3>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="flex items-center bottom-slider">
        <div><img src="../assets/img-2.png" alt="Slider" /></div>
        <div>
          <h3 class="slider-title q-pl-lg fw-900 q-my-none">해외 마케팅</h3>
        </div>
      </div>
    </swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

import { Autoplay, Pagination, Navigation } from "swiper/modules";
// Import Swiper styles
import "swiper/css";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay, Pagination, Navigation],
    };
  },
};
</script>
<style lang="scss">
.bottom-slider {
  padding: 16px;
  border-radius: 12px;
  background: rgba(255, 255, 255, 0.2);
  .slider-title {
    font-size: 24px;
    line-height: 36px;
  }
}
</style>
