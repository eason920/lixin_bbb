<template>
  <div class="relative">
    <section id="s7">
      <div class="s7tbox">
        <div class="s7tboxA" data-aos="fade-up" data-aos-duration="800">
          澳洲PTW精確指揮
          <p class="s7txt" data-aos="fade-up" data-aos-duration="800">
            國際團隊共譜建築世紀絕唱
          </p>
        </div>
        <div class="s7tboxB" data-aos="fade-up" data-aos-duration="800">
          世界上有二種建築，一種是PTW建築，一種不是。擁有132年水岸建築底蘊的澳洲PTW將居住空間當作城市藝術來創作，同時聚首日月潭涵碧樓、台中帝寶設計師王勝正、台北101燈光設計蘭克斯，共同擘劃碧潭首座結合波浪舞蹈藝術律動建築。看見「碧波白」，就看見台灣！
        </div>
      </div>
      <!-- PC -->
      <div class="s7box" v-if="!isMobile">
        <!-- <S7Card :obj="json.s7card[0]" /> -->
        <div class="s7item" data-aos="fade-up" data-aos-duration="800">
          <img class="s7pic" src="./S7/1.png" />
          <div class="s7txbox">
            <div class="s7title">
              <span>涵碧美學</span><span>公設設計</span>
            </div>
            <div class="s7name">王勝正</div>
            <p class="s7txt">
              代表作：<br />
              涵碧樓‧士林官邸<br />
              台中帝寶‧天母大境<br />
              鄉林皇居‧聯聚信義大廈
            </p>
          </div>
        </div>
        <div
          class="s7item"
          data-aos="fade-up"
          data-aos-duration="800"
          data-aos-delay="100"
        >
          <img class="s7pic" src="./S7/2.png" />
          <div class="s7txbox long">
            <div class="s7title">
              <span>建築巨擘</span><span>澳洲PTW 團隊</span>
            </div>
            <div class="s7name">Andrew Frost</div>
            <p class="s7txt">
              代表作：<br />
              北京水立方<br />
              杜拜 Palm Jebel<br />
              雪梨 Lumiere‧One Central Park
            </p>
          </div>
        </div>
        <div
          class="s7item"
          data-aos="fade-up"
          data-aos-duration="800"
          data-aos-delay="200"
        >
          <img class="s7pic" src="./S7/3.png" />
          <div class="s7txbox">
            <div class="s7title">
              <span>光雕之美</span><span>燈光設計</span>
            </div>
            <div class="s7name">蘭克斯燈光</div>
            <p class="s7txt">
              代表作：<br />
              台北101‧仁愛帝寶<br />
              W HOTEL‧澳門威尼斯酒店<br />
              遠企中心
            </p>
          </div>
        </div>
        <div
          class="s7item"
          data-aos="fade-up"
          data-aos-duration="800"
          data-aos-delay="300"
        >
          <img class="s7pic" src="./S7/4.png" />
          <div class="s7txbox">
            <div class="s7title">
              <span>豪宅御用</span><span>景觀設計</span>
            </div>
            <div class="s7name">大漢景觀 徐世萃</div>
            <p class="s7txt">
              代表作：<br />
              維多莉亞酒店<br />
              甲山林-城上城<br />
              墾丁凱薩大飯店
            </p>
          </div>
        </div>
      </div>

      <!-- MOBILE -->
      <swiper v-else :options="swiperOptionS7" ref="swiperS7">
        <swiper-slide>
          <div class="s7item">
            <img class="s7pic" src="./S7/1.png" />
            <div class="s7txbox">
              <div class="s7title">
                <span>涵碧美學</span><span>公設設計</span>
              </div>
              <div class="s7name">王勝正</div>
              <p class="s7txt">
                代表作：<br />
                涵碧樓‧士林官邸<br />
                台中帝寶‧天母大境<br />
                鄉林皇居‧聯聚信義大廈
              </p>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="s7item">
            <img class="s7pic" src="./S7/2.png" />
            <div class="s7txbox long">
              <div class="s7title">
                <span>建築巨擘</span><span>澳洲PTW 團隊</span>
              </div>
              <div class="s7name">Andrew Frost</div>
              <p class="s7txt">
                代表作：<br />
                北京水立方<br />
                杜拜 Palm Jebel<br />
                雪梨 Lumiere‧One Central Park
              </p>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="s7item">
            <img class="s7pic" src="./S7/3.png" />
            <div class="s7txbox">
              <div class="s7title">
                <span>光雕之美</span><span>燈光設計</span>
              </div>
              <div class="s7name">蘭克斯燈光</div>
              <p class="s7txt">
                代表作：<br />
                台北101‧仁愛帝寶<br />
                W HOTEL‧澳門威尼斯酒店<br />
                遠企中心
              </p>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="s7item">
            <img class="s7pic" src="./S7/4.png" />
            <div class="s7txbox">
              <div class="s7title">
                <span>豪宅御用</span><span>景觀設計</span>
              </div>
              <div class="s7name">大漢景觀 徐世萃</div>
              <p class="s7txt">
                代表作：<br />
                維多莉亞酒店<br />
                甲山林-城上城<br />
                墾丁凱薩大飯店
              </p>
            </div>
          </div>
        </swiper-slide>
        <template v-slot:button-prev>
          <div class="swiper-button-prev" @click="prevBtnS7"></div>
        </template>
        <template v-slot:button-next>
          <div class="swiper-button-next" @click="nextBtnS7"></div>
        </template>
      </swiper>
    </section>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

import { isMobile, isTablet } from '@/utils'

export default {
  name: 'section1',
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      isMobile,
      isTablet,
      // swiper v
      swiperOptionS7: {
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
    prevBtnS7() {
      this.$refs.swiperS7.$swiper.slidePrev()
    },
    nextBtnS7() {
      this.$refs.swiperS7.$swiper.slideNext()
    }
  },

  created() {},

  mounted() {},

  computed: {}
}
</script>

<style lang="sass" scoped>
@import "src/assets/style/myvar"
@media screen and (max-width: $bp-mb)
  $w: 28px
  .swiper-button-prev,
  .swiper-button-next
    width: $w
    height: $w
    border-radius: 50%
    background: #e0cca1
    top: 40vh
    &:after
      display: none!important
</style>

<style lang="scss" scoped>
.thumb-example {
  width: 376px;
  height: 376px;
  background-color: #fff;
}

// .swiper-container {
//   height: 100vh;
// }

.swiper-slide {
  background-position: center;
}
.swiper {
  margin-bottom: 10px;

  &.gallery-top {
    height: 80%;
    width: 100%;
  }
}
</style>

<style lang="sass" scoped>
@import "src/assets/style/myvar"
.s7box
  display: flex

.s7item
  letter-spacing: 1px
  line-height: 1.3
  display: flex
  flex-direction: column
  justify-items: flex-end

.s7pic
  width: 100%

.s7txbox
  padding-left: 30%
  &.long
    padding-left: 20%

.s7title
  display: flex
  padding: 12px 0
  span
    &:nth-child(odd)
      color: #c19943
      font-size: 21px
      padding-right: 10px
    &:nth-child(even)
      color: #000
      border-left: #777 1px solid
      font-size: 18px
      padding-left: 10px
.s7name
  color: #000
  font-size: 16px
  text-align: left
  padding: 0 0 12px

.s7txt
  clor: #000
  font-size: 12px
  text-align: left
@media screen and (min-width: $bp-pc)
  .s7box
    padding-top: 100px
  .s7item
    &:nth-child(even)
      // transform: translateY(-70px)
      position: relative
      top: -50px
@media screen and (max-width: $bp-mb)
  .s7item
    padding:
      left: 5%
      right: 15%
// --------------------------------
// --------------------------------
// --------------------------------
#s7
  background: #f2f2f2

.s7tbox
  color: #000
  letter-spacing: 1px
  text-align: left
.s7tboxA
  line-height: 1.7
  letter-spacing: 2px
.s7tboxB
  line-height: 2
@media screen and (min-width: $bp-pc)
  #s7
    padding: 5vw 5vw
  .s7tbox
    display: flex
    justify-content: space-between
  .s7tboxA
    font-size: 28px
    p
      font-size: 38px
  .s7tboxB
    line-height: 2.5
    font-size: 16px
    width: 40vw
@media screen and (max-width: $bp-mb)
  #s7
    padding-bottom: 15vh
  .s7tbox
    padding: 10vw
  .s7tboxA
    font-size: 20px
    padding-bottom: 25px
    p
      font-size: 23px
  .s7tboxB
    font-size: 16px
</style>
