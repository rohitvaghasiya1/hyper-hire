<template>
  <swiper
    :slides-per-view="'1.75'"
    :centeredSlides="true"
    :speed="500"
    :loop="true"
    navigation
    :modules="modules"
  >
    <swiper-slide>
      <div class="card text-center">
        <div class="card-image relative-position mb-4">
          <img src="../assets/profile.png" />
          <div class="flag absolute-bottom-right">
            <img src="../assets/flag.png" />
          </div>
        </div>
        <div class="card-body q-pt-md">
          <h3 class="card-title q-my-none q-pb-sm">Abhishek Gupta</h3>
          <p class="card-subtitle q-mb-none">마케팅 · 2y+</p>
          <ul class="badge-list">
            <li><p>마케팅 콘텐츠 제작</p></li>
            <li><p>인스타그램 관리</p></li>
            <li><p>트위터 관리</p></li>
            <li><p>블로그 글 작성</p></li>
          </ul>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="card text-center">
        <div class="card-image relative-position mb-4">
          <img src="../assets/profile.png" />
          <div class="flag absolute-bottom-right">
            <img src="../assets/flag.png" />
          </div>
        </div>
        <div class="card-body q-pt-md">
          <h3 class="card-title q-my-none q-pb-sm">Abhishek Gupta</h3>
          <p class="card-subtitle q-mb-none">마케팅 · 2y+</p>
          <ul class="badge-list">
            <li><p>마케팅 콘텐츠 제작</p></li>
            <li><p>인스타그램 관리</p></li>
            <li><p>트위터 관리</p></li>
            <li><p>블로그 글 작성</p></li>
          </ul>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="card text-center">
        <div class="card-image relative-position mb-4">
          <img src="../assets/profile.png" />
          <div class="flag absolute-bottom-right">
            <img src="../assets/flag.png" />
          </div>
        </div>
        <div class="card-body q-pt-md">
          <h3 class="card-title q-my-none q-pb-sm">Abhishek Gupta</h3>
          <p class="card-subtitle q-mb-none">마케팅 · 2y+</p>
          <ul class="badge-list">
            <li><p>마케팅 콘텐츠 제작</p></li>
            <li><p>인스타그램 관리</p></li>
            <li><p>트위터 관리</p></li>
            <li><p>블로그 글 작성</p></li>
          </ul>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="card text-center">
        <div class="card-image relative-position mb-4">
          <img src="../assets/profile.png" />
          <div class="flag absolute-bottom-right">
            <img src="../assets/flag.png" />
          </div>
        </div>
        <div class="card-body q-pt-md">
          <h3 class="card-title q-my-none q-pb-sm">Abhishek Gupta</h3>
          <p class="card-subtitle q-mb-none">마케팅 · 2y+</p>
          <ul class="badge-list">
            <li><p>마케팅 콘텐츠 제작</p></li>
            <li><p>인스타그램 관리</p></li>
            <li><p>트위터 관리</p></li>
            <li><p>블로그 글 작성</p></li>
          </ul>
        </div>
      </div>
    </swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/navigation";
// import required modules
import { Navigation } from "swiper/modules";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation],
    };
  },
};
</script>
<style lang="scss" scoped>
.card {
  padding: 36px;
  box-shadow: 0px 15px 24px 0px #0000001f;
  border-radius: 12px;
  background-color: #fff;
  box-shadow: 0px 15px 24px 0px #0000001f;
  .card-image {
    display: inline-block;
    img {
      margin: auto;
    }
  }
  .card-body {
    .card-title {
      font-size: 24px;
      font-weight: 900;
      line-height: 36px;
      text-align: center;
      color: #24252f;
    }
    .card-subtitle {
      font-size: 16px;
      font-weight: 900;
      color: #4a77ff;
      line-height: 24px;
      text-align: center;
    }
    .badge-list {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      padding-left: 0;
      margin-top: 20px;
      li {
        padding-bottom: 4px;
        p {
          font-size: 16px;
          color: #5e626f;
          display: block;
          padding: 4px 12px;
          border: 1px solid #c1c5cf;
          border-radius: 6px;
          margin-bottom: 0;
        }
      }
    }
  }
}
.swiper {
  width: 100%;
  height: 100%;
}
.swiper-slide-prev,
.swiper-slide-next {
  opacity: 0.5;
  transform: scale(0.85);
}
</style>
