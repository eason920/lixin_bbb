<template>
  <div class="relative">
    <section id="s9TT">
      <div class="s9t">
        <div class="s9tt" data-aos="fade-up">流著愛美基因的房子<span>歡迎對號入座</span></div>
        <div class="s9ts" data-aos="fade-up">
          生活面貌流瀉出空間主人舉手投足間的美學格調，「碧波白」名家窖藏空間中裝進紐約上城經典，有如一瓶精心釀造的拉菲紅酒，歷經最細緻的淬鍊與沉澱，細細品味生活醇厚餘韻，走進空間中的每一位主人，每天都將帶著鑑賞藝術品的心情--回家。
        </div>
        <div v-if="!isMobile" class="bblock" data-aos="fade-up"></div>
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
#s9TT
  padding: 8vw 5vw
  background-color: #f2f2f2
.s9t
  display: flex
  text-align: left
  justify-content: space-between
  position: relative
.s9tt
  font-size: 36px
  line-height: 1.3
  span
    display: block
  &:after
    content: ""
    position: absolute
    height: 1px
    margin: auto
    bottom: 0
    background: #707070
.s9ts
  font-size: 15px
  line-height: 2.2

@media screen and (min-width: $bp-pc)
  $b1: 3vw
  .s9t
    padding-bottom: $b1
    .bblock
      position: absolute
      right: $b1
      bottom: 0
  .s9tt
    position: relative
    &:after
      width: 100%
      bottom: $b1 * -1
  .s9ts
    padding-left: 10vw
    width: 45vw
@media screen and (max-width: $bp-mb)
  #s9TT
    padding: 15vw 10vw
  .s9t
    flex-direction: column
  .s9tt
    position: relative
    font-size: 18px
    line-height: 2
    margin-bottom: 20px
    &:after
      width: 30vw
      bottom: 10px
      right: 0
  .s9ts
    font-size: 12px
</style>
