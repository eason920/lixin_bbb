<template>
  <div>
    <swiper :options="swiperOptionTop" ref="swiperTop">
      <swiper-slide class="slide-1"><span>text</span></swiper-slide>
      <swiper-slide class="slide-2"><span>text</span></swiper-slide>
      <swiper-slide class="slide-3"><span>text</span></swiper-slide>
      <swiper-slide class="slide-4"><span>text</span></swiper-slide>
      <swiper-slide class="slide-5"><span>text</span></swiper-slide>
      <template v-slot:button-prev>
        <div class="swiper-button-prev" @click="prevBtn"></div>
      </template>
      <template v-slot:button-next>
        <div class="swiper-button-next" @click="nextBtn"></div>
      </template>
      <template v-slot:pagination>
        <div class="swiper-pagination" @click="nextBtn"></div>
      </template>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

export default {
  name: 'aaaa',
  title: 'Thumbs gallery with Two-way control',
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      swiperOptionTop: {
        loop: true,
        initialSlide: 0, // 最初 pic index
        spaceBetween: 10,
        autoplay: {
          delay: 1500,
          disableOnInteraction: true
        },
        speed: 800,
        grabCursor: true,
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
          type: 'bullets'
        },
        on: {
          slideChangeTransitionEnd: function() {
            // console.log(this.activeIndex) // 切換結束時，告訴我現在是第幾個slide
          }
        }
      }
    }
  },
  methods: {
    prevBtn() {
      this.$refs.swiperTop.$swiper.slidePrev()
    },
    nextBtn() {
      this.$refs.swiperTop.$swiper.slideNext()
    }
  }
}
</script>

<style lang="scss">
.thumb-example {
  width: 376px;
  height: 376px;
  background-color: #fff;
}

.swiper-container {
  height: 100vh;
}

.swiper-button-next {
  background: red;
}

.swiper-slide {
  background-position: center;
  span {
    position: absolute;
    left: 50%;
    bottom: 50%;
    z-index: 999;
    background: red;
    font-size: 100px;
    width: 200px;
  }

  &.slide-1 {
    background-image: url('./S8/1.jpg');
  }
  &.slide-2 {
    background-image: url('./S8/2.jpg');
  }
  &.slide-3 {
    background-image: url('./S8/3.jpg');
  }
  &.slide-4 {
    background-image: url('./S8/4.jpg');
  }
  &.slide-5 {
    background-image: url('./S8/5.jpg');
  }
}
.swiper {
  margin-bottom: 10px;

  &.gallery-top {
    height: 80%;
    width: 100%;
  }
  &.gallery-thumbs {
    height: 20%;
    width: 376px;
    box-sizing: border-box;
    padding: gap 0;
  }
  &.gallery-thumbs .swiper-slide {
    /* //等比例缩小 */
    opacity: 0.4;
    height: 68px;
    width: 68px;
    border: 1px solid #eee;
    background-size: contain;
  }
  &.gallery-thumbs .swiper-slide-active {
    opacity: 1;
  }
}
</style>
