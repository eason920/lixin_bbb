<template>
  <div>
    <!-- swiper1 -->
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

//js代码，可看注释，有更多的需求直接去官网看，文章后面有贴官网地址
<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

export default {
  name: 'swiper-example-thumbs-gallery',
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
        // loopedSlides: 5, // looped slides should be the same
        spaceBetween: 10,
        // 左右两边的点击事件
        // navigation: {
        //   nextEl: '.swiper-button-next',
        //   prevEl: '.swiper-button-prev'
        // },

        // notNextTick: true,
        // loop: true,
        // initialSlide: 0,
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
            console.log(this.activeIndex) // 切換結束時，告訴我現在是第幾個slide
          }
        }
      }
    }
  },
  // mounted() {
  //   // 可以使用swiper這個對象去使用swiper官網中的那些方法
  //   console.log('this is current swiper instance object', this.swiper)
  //   // this.swiper.slideTo(0, 0, false);

  //   this.$nextTick(() => {
  //     const swiperTop = this.$refs.swiperTop.$swiper
  //     const swiperThumbs = this.$refs.swiperThumbs.$swiper
  //     swiperTop.controller.control = swiperThumbs
  //     swiperThumbs.controller.control = swiperTop
  //   })
  // },
  methods: {
    prevBtn() {
      this.$refs.swiperTop.$swiper.slidePrev()
    },
    nextBtn() {
      this.$refs.swiperTop.$swiper.slideNext()
    }
  }

  // 這裏的this.swiper1是通過computed計算得來的
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
