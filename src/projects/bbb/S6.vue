<template>
  <div class="relative">
    <section id="s6">
      <div class="wave up">
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
            class="waveColorWhite"
            d="M0,132.7c406.1-5.2,421-162,1056.2-67.7c264.8,34.4,520.5,88.9,829,128.4c402.8,51.7,443.7,5.7,527.8-18.5c84-24.2,232.3-79.5,557-83.2c267-3,532,45,843,41V0.7L0,0.7L0,132.7z"
          />
        </svg>
      </div>
      <div class="s6m1">
        <div class="s6T" data-aos="fade-up" data-aos-duration="800">
          都市裡山水大景 <span>是您信手捻來的生活即景</span>
        </div>
        <div
          class="s6C"
          data-aos="fade-up"
          data-aos-duration="800"
          data-aos-delay="100"
        >
          與繁華之極的新店捷運站僅一步相隔，即能擁抱新北市最美的碧潭風景區，獨享27公傾蜿蜒悠然的水岸綠意，順著起伏低緩的和美山以及綿延的賞螢步道，一路漫步飽覽奇岩景緻。登上高處的碧亭，居高遠望盡收山水美景，碧潭吊橋俯瞰白天碧波與夜晚燐火，別有趣緻。多少台北人傾慕的碧潭之美，惟獨您無須特別空出行程，只因別人假日奢想，就是您日常生活的隨想。
        </div>
      </div>
      <div class="s6m2" v-if="isMobile">
        <img src="./S6/bg.jpg" />
      </div>
      <div class="wave" v-if="!isMobile">
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

<style lang="sass" scoped>
@import "src/assets/style/myvar"
#s6, .s6m2
  background:
    image: url("./S6/bg.jpg")

.s6m1
  color: #fff
  letter-spacing: 2px
.s6T
  font-size: 24px
  line-height: 1.5
  padding: 0 5px 5vw
  border-bottom: solid 1px #fff
  margin-bottom: 30px
  span
    display: block
.s6C
  font-size: 16px
  text-shadow: 1px 1px 3px rgba(0,0,0,.5), 1px 1px 3px rgba(0,0,0,.5)
  line-height: 1.9
@media screen and (min-width: $bp-pc)
  #s6
    height: 60vw
    background:
      position: 50%
      size: cover
      // size: contain
  .s6m1
    padding: 12vw 18vw
    display: flex
    flex-direction: column
    align-items: center
    .s6T
      font-size: 32px
      line-height: 1.5
      padding: 0 5px 2vw
      margin-bottom: 30px
      width: 70%
    .s6C
      font-size: 16px
      line-height: 2
@media screen and (max-width: $bp-mb)
  #s6
    background:
      size: 700%
      position: 0 0
  .s6m1
    padding: 23vw 10vw 20vw
    background-color: hsla(0,0%,100%,.05)
    backdrop-filter: blur(5px)
  .s6m2
    font-size: 0
    img
      width: 100%
</style>
