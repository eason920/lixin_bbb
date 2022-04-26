<template>
  <div class="relative">
    <section id="sec4">
      <div data-aos="fade-up" data-aos-duration="800">
        <h6>
          <p>摘下北新路地王桂冠</p>
          <p>在新店捷運站旁</p>
        </h6>
      </div>
      <div class="sec4-map">
        <div class="sec4-float" data-aos="fade-up" data-aos-duration="800">
          <div class="sec4-fitem is-1" @click="bIsOpen = true">
            <span>商圈之冠</span>
          </div>
          <div class="sec4-fitem is-2" @click="bIsOpen = true">
            <span>交通之冠</span>
          </div>
          <div class="sec4-fitem is-3" @click="bIsOpen = true">
            <span>捷運之冠</span>
          </div>
        </div>
        <img src="./S4/img.jpg" />
      </div>
      <div class="sec4-msg">
        <p data-aos="fade-up" data-aos-duration="800">
          想要順利取得碧潭畔、北新路新店捷運站旁的建地，並不是一件容易的事。新店最有價值的地段就屬北新路，與碧潭朝夕相處、幾近於零的遷出率、始終不墜的高行情、建地稀少的嚴峻條件下，門檻之高向來是新店市中心之冠。有幸入主的少數人，一輩子都捨不得搬離這個首善之區
        </p>
        <b class="bblock" data-aos="fade-up" data-aos-duration="800"></b>
      </div>
    </section>
    <div class="sec4lb" v-if="bIsOpen">
      <div class="sec4lb-close" @click="bIsOpen = false"></div>
      <div class="sec4lb-msg">
        <p>★1分鐘直上環快，15分鐘直達敦南、台北101信義商圈</p>
        <p>★5分鐘接軌新店、安坑雙交流道，南來北往市心機能全面精控</p>
      </div>
    </div>
  </div>
</template>

<style lang="sass" scoped>
@import "src/assets/style/myvar"
// --------------------------------
// --------------------------------
// --------------------------------
.sec4-msg
  color: #000
  padding: 5vw 6vw 5vw 7vw
  display: flex
  justify-content: space-between
  align-items: flex-end
  p
    text-align: left
    width: 45vw
    line-height: 1.5
    letter-spacing: 1px

@media screen and (max-width: $bp-mb)
  .sec4-msg
    padding: 5vh
    padding-right: 7vh
    p
      width: 100%
    b
      display: none

// --------------------------------
// --------------------------------
// --------------------------------
.sec4lb
  z-index: 9999
  background:
    image: url(./S4/1.jpg)
    position: 50% 0
    repeat: no-repeat
    color: rgba(200,200,200,.9)
  position: fixed
  top: 0
  right: 0
  bottom: 0
  left: 0
  margin: auto

$w: 35px
.sec4lb-close
  cursor: pointer
  position: fixed
  right: 20px
  top: 20px
  width: $w
  height: $w
  &:after, &:before
    background: #707070
    width: 135%
    height: 1px
    content: ''
    display: block
    // transform-origin: calc(50% + 1px)
    transition: .3s
  &:after
    transform: rotate(45deg)
    transform-origin: 0
  &:before
    transform: rotate(-45deg) translate(-10px, -10px)
    transform-origin: 100% 0
  &:hover
    &:after, &:before
      background: orange
.sec4lb-msg
  bottom: 40px
  left: 30px
  border-radius: 0 60px 60px 60px
  background: #000
  color: #fff
  position: fixed
  padding: 25px 50px
  p
    font:
      size: 16px
    text-align: left
    letter-spacing: 1px
    line-height: 1.5

@media screen and (min-width: $bp-pc)
  .sec4lb
    background:
      size: cover
      position: 50% 0
  .sec4lb-msg
    bottom: 40px
    left: 30px
    border-radius: 0 60px 60px 60px

@media screen and (max-width: $bp-mb)
  .sec4lb
    background:
      size: contain
      position: 0 50%
  .sec4lb-msg
    bottom: 40px
    left: 50%
    transform: translateX(-50%)
    border-radius: 0 60px 60px 60px
    width: 94vw
    padding: 30px

  .sec4lb-close
    &:after, &:before
      background: #333
// --------------------------------
// --------------------------------
// --------------------------------
#sec4
  background-color: #f2f2f2
  h6
    color: #333
    line-height: 1.5
    text-align: right
    font-weight: normal
    letter-spacing: 2px
    padding: 3vw 5vw 3vw 0
  &:after
    content: ''
    position: absolute
    width: 1px
    background: #707070
.sec4-map
  position: relative

//-
.sec4-float
  width: 100%
  position: absolute
  top: 0
  left: 0
  display: flex
  justify-content: space-around

.sec4-fitem
  box-shadow: 0 0 5px 0 rgb(0 0 0 / 75%)
  color: #000
  background: #fff
  display: flex
  justify-content: center
  align-items: center
  position: relative
  cursor: pointer
  span
    position: relative
    z-index: 1
  &:before
    content: ""
    position: absolute
    width: 100%
    height: 100%
    border: solid 5px #fff
    bottom: -12px
    right: -12px
    opacity: 0
    transition: .3s
  &:hover:before
    opacity: 1

  &.is-2
    transform: translateY(-6vh)

@media screen and (min-width: $bp-pc)
  #sec4
    &:after
      left: 4.5vw
      top: 0
      bottom: 5vw
      margin: auto
    h6
      font-size: 34px
  .sec4-map
    margin-top: 50px
    & > img
      width: 100vw

  //-
  .sec4-float
    padding-top: 30px
  .sec4-fitem
    height: 190px
    padding: 10px
    font-size: 26px
    line-height: 1.3
    width: 55px

@media screen and (max-width: $bp-mb)
  #sec4
    &:after
      top: 9vh
      right: 6vw
      bottom: 3vh
      margin: auto
    h6
      font-size: 21px
      padding:
        right: 15vw
        top: 20vw
  .sec4-map
    margin-top: 50px
    display: flex
    justify-content: center
    width: 100%
    height: 100%
    & > img
      height: 100%

  //-
  .sec4-float
    padding:
      top: 30px
      right: 6vw
  .sec4-fitem
    height: 134px
    padding: 10px
    font-size: 18px
    line-height: 1.3
    width: 48px
</style>

<script>

// import $ from "jquery";
// import {
//   ref,
//   // reactive,
//   watch,
//   // some
// } from "vue";
// const bIsOpen = ref(false);
// watch(bIsOpen, (val) => {
//   if (val) {
//     $("body").addClass("fixed");
//   } else {
//     $("body").removeClass("fixed");
//   }
// });

// @ is an alias to /src
import { isMobile, isTablet } from '@/utils'

export default {
  name: 'section1',

  data() {
    return {
      isMobile,
      isTablet,
      bIsOpen: false,
    }
  },

  methods: {},

  created() {},

  mounted() {},

  computed: {}
}
</script>
