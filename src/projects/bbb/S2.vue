<template>
  <div class="relative">
    <section id="sec2">
      <div class="sec2-l">
        <div
          class="sec2-title"
          data-aos-once="false"
          data-aos="fade-up"
          data-aos-duration="1500"
        >
          新店的國際名片
          <p>被維納斯親吻過的白派建築</p>
        </div>
        <div class="sec2-wapper">
          <div
            class="sec2-sub"
            data-aos-once="false"
            data-aos="fade-up"
            data-aos-delay="300"
            data-aos-duration="1500"
          >
            這是一座為夢想而生的建築，在外觀上被賦予獨一無二的生命和動感，這也是一座揚名全球的地標，榮獲國際建築設計六大獎項桂冠肯定，與紐約、倫敦、巴黎、柏林、義大利的建築巨作一同站上世界舞台
          </div>
          <div
            data-aos-once="false"
            data-aos="fade-up"
            data-aos-delay="600"
            data-aos-duration="1500"
          >
            <img class="sec2-img" src="./S2/logoall.png" />
          </div>
        </div>
      </div>
      <div class="sec2-r">
        <img class="sec2-sky" src="./S2/img.jpg" />
        <img class="sec2-build" src="./S2/img.png" />
      </div>
    </section>
    <section id="sec2-1">
      <div data-aos-once="false" data-aos="fade-up" data-aos-duration="800">
        <p>一生一遇 十全十美</p>
        <p>這個位址，見證您一生的輝煌</p>
      </div>
    </section>
  </div>
</template>

<style lang="sass" scoped>
@import "src/assets/style/myvar"
#sec2-1
  background-color: #f2f2f2
  line-height: 1.6
  color: #000
  // padding:
  //   bottom: 5vw
@media screen and (min-width: $bp-pc)
  #sec2-1
    font-size: 32px
  #sec2
    background-color: #f2f2f2
    display: flex
    // align-items: flex-end
    justify-content: space-between
    height: 90vh // 控總高
    padding:
      left: 5vw
      bottom: 5vh
      top: 5vh
    & > div
      width: 50%
  .sec2-l
    text-align: left
    padding: 10vh 5vw 0
    color: #000
  .sec2-title
    font:
      size: 2.2vw
    letter-spacing: .5vw
    padding:
      bottom: 12vh
    p
      padding-top: 5px
  .sec2-wapper
    padding-right: 9vw
  .sec2-sub
    font:
      size: 1vw
    line-height: 2
    letter-spacing: .3vw
    padding-bottom: 2vw
  .sec2-img
    width: 100%
    display: block

  // right
  .sec2-r
    height: 100%
    position: relative
    overflow: hidden
    border-radius: 50% 50% 0
    img
      // height: 100%
      width: 100%
      position: absolute
      left: 0
  .sec2-sky
    top: 0
  .sec2-build
    bottom: 0
    z-index: 1

@media screen and (min-width: 1600px)
  #sec2
    height: 110vh // 控總高

@media screen and (max-width: $bp-mb)
  #sec2-1
    font-size: 21px
    padding: 10vw 0 3vw
  #sec2
    background-color: #f2f2f2
    display: flex
    flex-direction: column
    align-items: flex-end
    padding:
      top: 10vh
  .sec2-l
    order: 2
    text-align: left
    padding: 10vh 10vw 0
    color: #000
    width: 100%
  .sec2-title
    font:
      size: 5vw
    letter-spacing: 1vw
    padding:
      bottom: 10vh
    p
      padding-top: 5px
  .sec2-wapper
    // padding-right: 9vw
  .sec2-sub
    font:
      size: 4vw
    line-height: 2
    letter-spacing: 1vw
    padding-bottom: 8vh
  .sec2-img
    width: 100%
    display: block

  // right
  .sec2-r
    order: 1
    height: 60vh
    position: relative
    overflow: hidden
    border-radius: 50% 50% 0
    width: 90vw
    img
      // height: 100%
      width: 100%
      position: absolute
      left: 0
  .sec2-sky
    top: 0
  .sec2-build
    bottom: 0
    z-index: 1
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
