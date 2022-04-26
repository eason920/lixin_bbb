<template>
  <div class="relative">
    <section id="s5-1">
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
            class="waveColorGray"
            d="M0,132.7c406.1-5.2,421-162,1056.2-67.7c264.8,34.4,520.5,88.9,829,128.4c402.8,51.7,443.7,5.7,527.8-18.5c84-24.2,232.3-79.5,557-83.2c267-3,532,45,843,41V0.7L0,0.7L0,132.7z"
          />
        </svg>
      </div>
      <div class="bblock" data-aos="fade-in" data-aos-duration="800"></div>
    </section>
    <section id="s5">
      <br />
      <div class="s51">
        <div class="s51T" data-aos="fade-up" data-aos-duration="800">
          碧潭上英姿風骨
          <p>30層SRC鋼骨制震地標</p>
        </div>
        <div
          class="s51Sub"
          v-if="!isMobile || bMbOpen"
          data-aos="fade-up"
          data-aos-duration="800"
        >
          無可取代的地標，最高層視野、最安全鋼骨、最頂級公設，「碧波白」融合大自然線條，以凌空30層律動建築地標君臨碧潭，與台北101同級制震鋼骨，讓大直仰望，與信義並肩，當代最波瀾壯闊的建築思潮，氣度格局連陽明都艷羨。無限高度、無限胸襟，唯有少數成功人士得以一窺堂奧。
        </div>
        <div v-if="isMobile" class="s51Subm">
          <h6 data-aos="fade-up" data-aos-duration="800">
            碧潭唯一SRC鋼骨建築 X 台北101同級建材
          </h6>
          <p v-if="bMbOpen" data-aos="fade-up" data-aos-duration="800">
            全棟建築結構以抗震耐火的SRC鋼骨嚴密施工，強化鋼筋續接處安全，特別採用最高等級SA級摩擦壓接續接器，與台北101同級，同時在斷面以跳接工法避免地震橫向破壞，達到最佳耐震力。
          </p>
          <h6 data-aos="fade-up" data-aos-duration="800">
            萬鎊混擬土 X 筏式基礎 承重抗壓
          </h6>
          <p v-if="bMbOpen" data-aos="fade-up" data-aos-duration="800">
            嚴選上市公司力泰水泥生產之優良混擬土，經ISO品質認證，柱內混擬土強度8000磅(psi)~10000磅(psi)，比一般工地高出約4000~6000磅以上。地基則以連續壁、筏式基礎施工，深入岩盤耐震加倍，在美景地王中靜享舒適穩固的安全堡壘。
          </p>
          <b v-if="!bMbOpen" @click="bMbOpen = true">+</b>
        </div>
      </div>
      <div
        class="s52"
        data-aos="fade-up"
        data-aos-delay="300"
        data-aos-duration="800"
      >
        <img src="./S5/img2.png" />
      </div>
      <div class="s53">
        <div
          class="s53p"
          data-aos="fade-up"
          data-aos-duration="800"
          data-aos-delay="100"
        >
          <img v-if="!isMobile" src="./S5/img1.png" />
          <img v-else src="./S5/img1m.png" />
        </div>
        <div class="s53t">
          <div v-if="!isMobile" class="s5bx2Outer">
            <div class="s5bx2">
              <h6 data-aos="fade-up" data-aos-duration="800">
                碧潭唯一SRC鋼骨建築 X 台北101同級建材
              </h6>
              <p data-aos="fade-up" data-aos-duration="800">
                全棟建築結構以抗震耐火的SRC鋼骨嚴密施工，強化鋼筋續接處安全，特別採用最高等級SA級摩擦壓接續接器，與台北101同級，同時在斷面以跳接工法避免地震橫向破壞，達到最佳耐震力。
              </p>
            </div>
            <div class="s5bx2">
              <h6 data-aos="fade-up" data-aos-duration="800">
                萬鎊混擬土 X 筏式基礎 承重抗壓
              </h6>
              <p data-aos="fade-up" data-aos-duration="800">
                嚴選上市公司力泰水泥生產之優良混擬土，經ISO品質認證，柱內混擬土強度8000磅(psi)~10000磅(psi)，比一般工地高出約4000~6000磅以上。地基則以連續壁、筏式基礎施工，深入岩盤耐震加倍，在美景地王中靜享舒適穩固的安全堡壘。
              </p>
            </div>
          </div>
          <div class="s5bx6Outer">
            <div
              class="s5bx6"
              data-aos="fade-up"
              data-aos-duration="800"
              data-aos-delay="200"
            >
              <div class="s5bx6t">
                結構升級<img src="./S5/icon.png" />
              </div>
              <p>全棟鋼材用料達1萬噸，約為一般建案一倍之多</p>
            </div>
            <div
              class="s5bx6"
              data-aos="fade-up"
              data-aos-duration="800"
              data-aos-delay="300"
            >
              <div class="s5bx6t">
                安全升級<img src="./S5/icon.png" />
              </div>
              <p>日式工法搭配SA壓接鋼筋續接器，強化續接處</p>
            </div>
            <div
              class="s5bx6"
              data-aos="fade-up"
              data-aos-duration="800"
              data-aos-delay="400"
            >
              <div class="s5bx6t">
                強度升級<img src="./S5/icon.png" />
              </div>
              <p>鋼板厚度達5-7公分，較坊間一般建案鋼板厚實</p>
            </div>
            <div
              class="s5bx6"
              data-aos="fade-up"
              data-aos-duration="800"
              data-aos-delay="500"
            >
              <div class="s5bx6t">
                耐震升級<img src="./S5/icon.png" />
              </div>
              <p>採世界級領先工法連續壁與筏式施工，深入岩盤</p>
            </div>
            <div
              class="s5bx6"
              data-aos="fade-up"
              data-aos-duration="800"
              data-aos-delay="600"
            >
              <div class="s5bx6t">
                保障升級<img src="./S5/icon.png" />
              </div>
              <p>鋼骨採用與台北101相同最高等級中鋼鋼骨原料</p>
            </div>
            <div
              class="s5bx6"
              data-aos="fade-up"
              data-aos-duration="800"
              data-aos-delay="700"
            >
              <div class="s5bx6t">
                抗壓升級<img src="./S5/icon.png" />
              </div>
              <p>使用1萬磅力泰混凝土較一般工地高4000-5000磅</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="sass" scoped>
@import "src/assets/style/myvar"
#s5-1
  background: #fff
  display: flex
  justify-content: flex-end
  align-items: flex-end
  padding:
    right: 6vw
    bottom: 1vh
  overflow-y: visible
  .bblock
    position: absolute
    right: 6vw
    bottom: 0
@media screen and (min-width: $bp-pc)
  #s5-1
    height: 200px

@media screen and (max-width: $bp-mb)
  #s5-1
    height: 100px
    .bblock
      display: none
// --------------------------------
// --------------------------------
.wave.up
  bottom: auto
  top: -1px
#s5
  background: #fff
  position: relative
  display: flex
  flex-wrap: wrap
  padding:
    left: 5vw
    right: 5vw
.s51
  width: 50vw
  & > *
    text-align: left
  .s51T
    color: #000
    letter-spacing: 1px
    line-height: 1.5
  .s51Sub
    color: #000
    letter-spacing: 1px
    line-height: 2
    font-size: 16px
.s52
  width: 50vw
  img
    width: 100%
.s53
  display: flex
  .s5bx6Outer
    display: flex
    flex-wrap: wrap
    .s5bx6
      width: 50%
      text-align: left
      margin-bottom: 30px
      .s5bx6t
        display: flex
        align-items: center
        font-size: 21px
        margin-bottom: 5px
        img
          width: 30px
          transform: translateY(-2px)
          margin-left: 7px
      p
        font-size: 12px
        letter-spacing: 1px

@media screen and (min-width: $bp-pc)
  .s51, .s52
    width: calc(50%)
  .s51
    .s51T
      font-size: 42px
      margin-bottom: 40px
    .s51Sub
      width: 70%
  .s52
    img
      width: 100%
  .s53
    padding: 80px 0
    .s53p
      width: 40%
      img
        width: 100%
    .s53t
      width: 60%
      padding-left: 80px
      .s5bx2Outer
        text-align: left
        color: #000
        letter-spacing: 1px
        .s5bx2
          padding-bottom: 30px
        h6
          font:
            size: 21px
            weight: lighter
          padding-bottom: 10px
        p
          font-size: 15px
          line-height: 1.7
@media screen and (max-width: $bp-mb)
  .s51
    width: 100%
    order: 1
    .s51T
      font-size: 24px
      margin-bottom: 18px
    .s51Sub
      margin-bottom: 40px
    .s51Subm
      color: #000
      padding-bottom: 40px
      h6
        font-weight: normal
        line-height: 1.7
      p
        padding: 6px 0 40px
        font-size: 12px
        letter-spacing: 1px
        line-height: 1.5
      b
        margin-top: 20px
        background: #f2f2f2
        font:
          weight: lighter
          size: 50px
        color: #707070
        padding: 3px 0 7px
        display: block
        text-align: center
  .s52
    order: 3
    margin-bottom: 60px
    width: 100%
    img
      width: 100%
  .s53
    order: 2
    justify-content: space-between
    margin-bottom: 60px
    .s53p
      order: 2
      width: 45%
      img
        width: 100%
    .s53t
      order: 1
      width: 45%

    .s5bx6Outer
      .s5bx6
        width: 100%
        .s5bx6t
          img
            width: 30px
            transform: translateY(-2px)
            margin-left: 7px
        p
          line-height: 1.5
</style>

<script>
// @ is an alias to /src
import { isMobile, isTablet } from '@/utils'

export default {
  name: 'section1',

  data() {
    return {
      isMobile,
      isTablet,
      bMbOpen: false
    }
  },

  methods: {},

  created() {},

  mounted() {},

  computed: {}
}
</script>
