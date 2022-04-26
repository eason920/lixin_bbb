<template>
  <div class="relative">
    <section id="s9">
      <swiper
        v-if="is38"
        :options="swiperOption38"
        ref="swiper38"
        class="is-38"
      >
        <swiper-slide>
          <div class="s9item"></div>
        </swiper-slide>
        <swiper-slide>
          <div class="s9item"></div>
        </swiper-slide>
        <swiper-slide>
          <div class="s9item"></div>
        </swiper-slide>
        <template v-slot:button-prev>
          <div class="swiper-button-prev s9pv" @click="prevBtn38"></div>
        </template>
        <template v-slot:button-next>
          <div class="swiper-button-next s9pv" @click="nextBtn38"></div>
        </template>
        <template v-slot:pagination>
          <div class="swiper-pagination"></div>
        </template>
      </swiper>
      <swiper v-else :options="swiperOption45" ref="swiper45" class="is-45">
        <swiper-slide>
          <div class="s9item"></div>
        </swiper-slide>
        <swiper-slide>
          <div class="s9item"></div>
        </swiper-slide>
        <swiper-slide>
          <div class="s9item"></div>
        </swiper-slide>
        <template v-slot:button-prev>
          <div class="swiper-button-prev s9pv" @click="prevBtn45"></div>
        </template>
        <template v-slot:button-next>
          <div class="swiper-button-next s9pv" @click="nextBtn45"></div>
        </template>
        <template v-slot:pagination>
          <div class="swiper-pagination"></div>
        </template>
      </swiper>
      <div class="s9Msg" v-if="is38">
        <div class="s9MB">
          <div class="bblock" data-aos="fade-up" data-aos-duration="800"></div>
          <div class="s9MT" data-aos="fade-up" data-aos-duration="800">
            38坪
            <p>如詩行旅</p>
          </div>
          <div class="s9MS" data-aos="fade-up" data-aos-duration="800">
            多元獨特的個人風格設計，符合城市菁英需求的複合生活空間，可以是個人工作室，可以是雙人甜蜜合居，可以是一家人的換屋首選。
          </div>
        </div>
      </div>
      <div class="s9Msg" v-else>
        <div class="s9MB">
          <div class="bblock" data-aos="fade-up" data-aos-duration="800"></div>
          <div class="s9MT" data-aos="fade-up" data-aos-duration="800">
            45坪
            <p>
              大器雍容
            </p>
          </div>
          <div class="s9MS" data-aos="fade-up" data-aos-duration="800">
            優雅舒適大宅大器空間，大面開窗主臥採光通透，錦鋐氣密隔音防潮，開放式客餐廳，在家料理私廚美饌，享受宴客聚餐樂趣
          </div>
        </div>
      </div>
      <div class="s9Switch" @click="is38 = !is38">
        <div class="s9SBox">
          <div class="s9Item" :class="[{ on: is38 }]">38<span>坪</span></div>
          <div class="s9Item" :class="[{ on: !is38 }]">45<span>坪</span></div>
        </div>
      </div>
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
      is38: true,
      swiperOption38: {
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
      },
      swiperOption45: {
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
    prevBtn38() {
      this.$refs.swiper38.$swiper.slidePrev()
    },
    nextBtn38() {
      this.$refs.swiper38.$swiper.slideNext()
    },
    prevBtn45() {
      this.$refs.swiper45.$swiper.slidePrev()
    },
    nextBtn45() {
      this.$refs.swiper45.$swiper.slideNext()
    }
  }
}
</script>

<style lang="scss">
@import 'src/assets/style/myvar';
#s9 {
  .swiper-container-horizontal > .swiper-pagination-bullets {
    top: auto;
    bottom: 14px;
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
  #s9 {
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
.is-38
  .swiper-slide
    &:nth-child(1), &:nth-child(4)
      background-image: url('./S9/38-1.jpg')

    &:nth-child(2), &:nth-child(5)
      background-image: url('./S9/38-2.jpg')

    &:nth-child(3), &:nth-child(6)
      background-image: url('./S9/38-3.jpg')
.is-45
  .swiper-slide
    &:nth-child(1), &:nth-child(4)
      background-image: url('./S9/45b-1.jpg')

    &:nth-child(2), &:nth-child(5)
      background-image: url('./S9/45b-2.jpg')

    &:nth-child(3), &:nth-child(6)
      background-image: url('./S9/45b-3.jpg')

@media screen and (min-width: $bp-pc)
  .swiper-container,
  .swiper-wrapper,
  .swiper-slide,
  .s9item
    height: 60vw
    max-height: 70vh
@media screen and (max-width: $bp-mb) and (orientation: portrait)
  .swiper-container,
  .swiper-wrapper,
  .swiper-slide,
  .s9item
    height: 30vh

@media screen and (max-width: $bp-mb) and (orientation: landscape)
  .swiper-container,
  .swiper-wrapper,
  .swiper-slide,
  .s9item
    height: 100vh

@media screen and (orientation: landscape)
  .s9pic
    width: 100%
@media screen and (orientation: portrait)
  .s9pic
    height: 100%

.s9item
  position: relative

.s9tx
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
  .s9tx
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

// --------------------------------
// --------------------------------
.s9Switch
  position: absolute
  top: 30px
  left: 50%
  transform: translateX(-50%)
  background: rgba(200,200,200,.4)
  padding: 8px
  border-radius: 23px
  z-index: 10

.s9SBox
  border-radius: 15px
  background-color: #fff
  display: flex
  // flex-direction: column
.s9Item
  border-radius: 15px
  width: 85px
  padding: 12px 0
  display: flex
  justify-content: center
  align-items: flex-end
  font-size: 26px
  cursor: pointer
  user-select: none
  span
    font-size: 16px
    margin-left: 3px
  &.on
    width: 100px
    background-color: #000
    color: #fff
@media screen and (max-width: $bp-mb)
  $f: 18px
  .s9Switch
    top: 10px
  .s9Item
    width: 70px
    padding: 12px 0
    font-size: $f
    span
      font-size: $f
    &.on
      width: 85px
      background-color: #000
      color: #fff

// --------------------------------
// --------------------------------
$smt: 4.5vw
.s9Msg
  background: #f2f2f2
  padding: $smt 5vw
  position: relative
  .bblock
    position: absolute
    top: $smt
.s9MB
  display: flex
  justify-content: space-between
  text-align: left
  padding-top: $smt
  positipn: relative
  color: #000
  &:after
    content: ""
    position: absolute
    height: 1px
    width: 40vw
    background: #000
    top: $smt
    right: 5vw
.s9MT
  font-size: 42px
  line-height: 1.3
  letter-spacing: 5px
  p
    letter-spacing: 5px
.s9MS
  line-height: 2
  width: 25vw

@media screen and (max-width: $bp-mb)
  $smt2: 15px
  .s9Msg
    padding:
      left: 10vw
      right: 10vw
    .bblock
      display: none
  .s9MB
    flex-direction: column
    padding-top: $smt2
    &:after
      display: none
  .s9MT
    font-size: 21px
    line-height: 2
    letter-spacing: 5px
    padding-bottom: 20px
    p
      letter-spacing: 5px
  .s9MS
    font-size: 15px
    width: 100%
</style>
