<template>
  <div class="relative">
    <section id="s8">
      <swiper :options="swiperOptionS8" ref="swiperS8">
        <swiper-slide>
          <div class="s8item">
            <div class="s8tx">
              <p>尊榮雙門廳</p>
              <span>最頂級的入門之道，回家就是尊榮禮遇</span>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="s8item">
            <div class="s8tx">
              <p>尊榮雙門廳</p>
              <span>最頂級的入門之道，回家就是尊榮禮遇</span>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="s8item">
            <div class="s8tx">
              <p>尊榮雙門廳</p>
              <span>最頂級的入門之道，回家就是尊榮禮遇</span>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="s8item">
            <div class="s8tx">
              <p>尊榮雙門廳</p>
              <span>最頂級的入門之道，回家就是尊榮禮遇</span>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="s8item">
            <!-- <img class="s8pic" src="./S8/5.jpg" /> -->
            <div class="s8tx">
              <p>尊榮雙門廳</p>
              <span>最頂級的入門之道，回家就是尊榮禮遇</span>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="s8item">
            <!-- <img class="s8pic" src="./S8/6.jpg" /> -->
            <div class="s8tx">
              <p>尊榮雙門廳</p>
              <span>最頂級的入門之道，回家就是尊榮禮遇</span>
            </div>
          </div>
        </swiper-slide>
        <template v-slot:button-prev>
          <div class="swiper-button-prev s8pv" @click="prevBtnS8"></div>
        </template>
        <template v-slot:button-next>
          <div class="swiper-button-next s8pv" @click="nextBtnS8"></div>
        </template>
        <template v-slot:pagination>
          <div class="swiper-pagination"></div>
        </template>
      </swiper>
    </section>
  </div>
</template>

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
      swiperOptionS8: {
        loop: true,
        initialSlide: 0, // 最初 pic index
        spaceBetween: 0,
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
    prevBtnS8() {
      this.$refs.swiperS8.$swiper.slidePrev()
    },
    nextBtnS8() {
      this.$refs.swiperS8.$swiper.slideNext()
    }
  }
}
</script>

<style lang="scss">
@import 'src/assets/style/myvar';
#s8 {
  .swiper-container-horizontal > .swiper-pagination-bullets {
    bottom: auto;
    top: 15px;
  }
}
.swiper-container-horizontal
  > .swiper-pagination-bullets
  .swiper-pagination-bullet {
  width: 50px;
  height: 12px;
  border-radius: 0;
  border: solid 2px #f2f2f2;
  &.swiper-pagination-bullet-active {
    background: #f2f2f2;
  }
}

@media screen and (max-width: $bp-mb) {
  #s8 {
    .swiper-container-horizontal > .swiper-pagination-bullets {
      display: none;
    }
  }
  .swiper-button-prev,
  .swiper-button-next {
    width: 30px !important;
    top: 50%;
    transform: translateY(-50%);
    &:after {
      font-size: 20px;
    }
  }
}
//-- ----------------------------
.thumb-example {
  width: 376px;
  height: 376px;
  background-color: #fff;
}

.swiper-button-prev,
.swiper-button-next {
  width: 50px;
  height: 80px;
  &:after {
    color: #fff;
    text-shadow: 0px 0px 5px rgba(0, 0, 0, 0.5), 0px 0px 5px rgba(0, 0, 0, 0.5);
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

<style lang="sass" scoped>
@import "src/assets/style/myvar"
.swiper-slide
  background:
    position: center
    size: cover
  &:nth-child(1), &:nth-child(7)
    background-image: url('./S8/1.jpg')

  &:nth-child(2), &:nth-child(8)
    background-image: url('./S8/2.jpg')

  &:nth-child(3), &:nth-child(9)
    background-image: url('./S8/3.jpg')

  &:nth-child(4)
    background-image: url('./S8/4.jpg')

  &:nth-child(5)
    background-image: url('./S8/5.jpg')

  &:nth-child(6)
    background-image: url('./S8/6.jpg')

@media screen and (min-width: $bp-pc)
  .swiper-container,
  .swiper-wrapper,
  .swiper-slide,
  .s8item
    height: 60vw
    max-height: 70vh
@media screen and (max-width: $bp-mb) and (orientation: portrait)
  .swiper-container,
  .swiper-wrapper,
  .swiper-slide,
  .s8item
    height: 30vh

@media screen and (max-width: $bp-mb) and (orientation: landscape)
  .swiper-container,
  .swiper-wrapper,
  .swiper-slide,
  .s8item
    height: 100vh

@media screen and (orientation: landscape)
  .s8pic
    width: 100%
@media screen and (orientation: portrait)
  .s8pic
    height: 100%

.s8item
  position: relative

.s8tx
  height: 30px
  position: absolute
  left: 5vw
  bottom: 20px
  color: #fff
  text-shadow: 0 0 5px rgba(0,0,0,.5), 0 0 5px rgba(0,0,0,.5)
  display: flex
  align-items: center
  & > *
    height: 100%
    display: flex
    align-items: center
  p
    font-size: 24px
    padding-right: 15px
    margin-right: 15px
    border-right: solid 2px #fff
  span
    font-size: 18px

@media screen and (max-width: $bp-mb)
  .s8tx
    height: auto
    bottom: 20px
    display: flex
    flex-direction: column
    align-items: flex-start
    & > *
      height: 100%
      display: flex
      align-items: center
    p
      font-size: 18px
      border-right: none
    span
      margin-top: 8px
      font-size: 14px
</style>
