<template>
  <div class="relative">
    <section id="sec1">
      <img v-if="!isMobile" class="sec1-bgimg" src="./S1/bg.jpg" />
      <img v-else class="sec1-bgimg" src="./S1/bg_m.jpg" />
      <div
        class="sec1-bgbuild"
        data-aos-once="false" data-aos="fade-up"
        data-aos-duration="800"
      >
        <img v-if="!isMobile" src="./S1/img.png" />
        <img v-else src="./S1/img_m.png" />
      </div>
      <div class="sec1-title">
        <div data-aos-once="false" data-aos="fade-up" data-aos-duration="1500">
          <img class="sec1-title-img" src="./S1/logo.png" />
        </div>
        <div
          class="sec1-title-sub"
          data-aos-once="false" data-aos="fade-up"
          data-aos-duration="1200"
        >
          台灣唯一<span class="sec1-title-sub-span"
            >七大國際建築設計獎得主</span
          >
        </div>
      </div>
      <div class="wave">
        <!-- <img src="./S1/wave.svg" /> -->
        <svg
          version="1.1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          x="0px"
          y="0px"
          viewBox="0 0 3813 217"
          style="enable-background:new 0 0 3813 217;"
          xml:space="preserve"
        >
          <path
            class="waveColorGray"
            d="M3813,85c-406.1,5.2-421,162-1056.2,67.7c-264.8-34.4-520.5-88.9-829-128.4C1525-27.4,1484.1,18.6,1400,42.8c-84,24.2-232.3,79.5-557,83.2C576,129,311,81,0,85v132h3813V85z"
          />
        </svg>
      </div>
    </section>
  </div>
</template>

<style lang="sass" scoped>
.wave
  bottom: -1px
@import "src/assets/style/myvar"
@media screen and (min-width: $bp-pc)
  #sec1
    height: 56.25vw
  .sec1-title
    position: absolute
    top: 15vw
    right: 17vw
    padding-top: 0
    font-size: 1.9vw
    width: 35vw
    color: #fff
    letter-spacing: 2px

  .sec1-title-img
    width: 20vw
    margin: auto auto 1.04167vw

  .sec1-bgimg,
  .sec1-bgbuild
    display: block
    height: 100%
    position: absolute
    top: 0
    left: 0
@media screen and (max-width: $bp-mb)
  #sec1
    height: calc( 100vh - 63px )
  .sec1-title
    position: absolute
    top: 35vw
    right: 50%
    transform: translateX(50%)
    padding-top: 0
    font-size: 5vw
    width: 90vw
    color: #fff
    letter-spacing: 1vw
    z-index: 3
    line-height: 1.5

  .sec1-title-img
    width: 65vw
    margin: auto auto 2vh

  .sec1-title-sub-span
    display: block

  .sec1-bgimg,
  .sec1-bgbuild
    display: block
    position: absolute
    left: 0
  .sec1-bgimg
    height: 100vh
    bottom: 0
    z-index: 1
  .sec1-bgbuild
    width: 100%
    bottom: 15vh
    z-index: 2
    img
      display: block
      transform: translateY(35vh)
      height: auto
</style>

<script>
// @ is an alias to /src
import { isMobile, isTablet } from '@/utils'

export default {
  name: 'section1',

  data() {
    return {
      isMobile,
      isTablet
    }
  },

  methods: {},

  created() {},

  mounted() {},

  computed: {}
}
</script>
