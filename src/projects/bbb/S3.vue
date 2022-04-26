<template>
  <div class="relative">
    <section id="sec3">
      <div class="wave up no-ani">
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
      <div class="sec3-imgbox">
        <img v-if="!isMobile" src="./S3/bg.jpg" />
        <img v-else src="./S3/bgm.jpg" />
      </div>
      <div class="cbox">
        <div :class="`cbox-box is-${nCurrent}`">
          <div class="cbox-iouter first">
            <div class="cbox-item" @click="fnCCheck(1)">
              <div class="cbox-i" :class="[{ on: nCurrent === 1 && bOn }]">
                <div class="cbox-txt">多角<span>視野</span></div>
                <div class="cbox-n">1</div>
                <div class="cbox-p">
                  <span>
                    離101最近國家級生態保護區，坐擁碧潭、和美山、灣潭，親近知名風景是別人假日奢想，卻是您日常生活的隨想
                  </span>
                </div>
              </div>
            </div>
          </div>
          <div class="cbox-iouter">
            <div class="cbox-item" @click="fnCCheck(2)">
              <div class="cbox-i" :class="[{ on: nCurrent === 2 && bOn }]">
                <div class="cbox-txt">絕版<span>地王</span></div>
                <div class="cbox-n">2</div>
                <div class="cbox-p">
                  <span>
                    碧潭滿席中絕版地王，台北都會區內有山有水，限量土地增值力，有錢也不見得買得到
                  </span>
                </div>
              </div>
            </div>
          </div>
          <div class="cbox-iouter">
            <div class="cbox-item" @click="fnCCheck(3)">
              <div class="cbox-i" :class="[{ on: nCurrent === 3 && bOn }]">
                <div class="cbox-txt">國際<span>地標</span></div>
                <div class="cbox-n">3</div>
                <div class="cbox-p">
                  <span>
                    澳洲132年水岸建築團隊PTW，以白色波浪山水曲線，跨海擘建30層和碧潭比美的水岸國際地標建築
                  </span>
                </div>
              </div>
            </div>
          </div>
          <div class="cbox-iouter">
            <div class="cbox-item" @click="fnCCheck(4)">
              <div class="cbox-i" :class="[{ on: nCurrent === 4 && bOn }]">
                <div class="cbox-txt">山水<span>版圖</span></div>
                <div class="cbox-n">4</div>
                <div class="cbox-p">
                  <span>
                    1分鐘直上環快，15分鐘敦南、信義雙商圈，5分鐘新店、安坑雙交流道，台北都心最近山水版圖
                  </span>
                </div>
              </div>
            </div>
          </div>
          <div class="cbox-iouter">
            <div class="cbox-item" @click="fnCCheck(5)">
              <div class="cbox-i" :class="[{ on: nCurrent === 5 && bOn }]">
                <div class="cbox-txt">換屋<span>首選</span></div>
                <div class="cbox-n">5</div>
                <div class="cbox-p">
                  <span>
                    38-45坪多元獨特的個人風格設計，完美符合現代需求的複合生活空間，可以共渡雙人甜蜜時光，更可以同享天倫合樂，是一家人的換屋首選。
                  </span>
                </div>
              </div>
            </div>
          </div>
          <div class="cbox-iouter">
            <div class="cbox-item" @click="fnCCheck(6)">
              <div class="cbox-i" :class="[{ on: nCurrent === 6 && bOn }]">
                <div class="cbox-txt">食衣<span>住行</span></div>
                <div class="cbox-n">6</div>
                <div class="cbox-p">
                  <span>
                    正北新路大道上，列席碧潭觀光市集、肯德基光明街雙商圈，散步1分鐘大潤發，食衣住行機能貼身近擁
                  </span>
                </div>
              </div>
            </div>
          </div>
          <div class="cbox-iouter">
            <div class="cbox-item" @click="fnCCheck(7)">
              <div class="cbox-i" :class="[{ on: nCurrent === 7 && bOn }]">
                <div class="cbox-txt">首席<span>設計</span></div>
                <div class="cbox-n">7</div>
                <div class="cbox-p">
                  <span>
                    涵碧樓御用首席設計師王勝正師法自然、借山引水，繼日月潭後，為碧潭量身訂做涵碧美學御所，回到家也回到藝術品
                  </span>
                </div>
              </div>
            </div>
          </div>
          <div class="cbox-iouter">
            <div class="cbox-item" @click="fnCCheck(8)">
              <div class="cbox-i" :class="[{ on: nCurrent === 8 && bOn }]">
                <div class="cbox-txt">SRC<span>鋼骨</span></div>
                <div class="cbox-n">8</div>
                <div class="cbox-p">
                  <span>
                    碧潭畔上的英姿風骨，全棟SRC制震鋼骨，採用同台北101最高等級SA鋼筋續接器，萬噸鋼骨搭配萬磅混凝土，為一般建案一倍之多
                  </span>
                </div>
              </div>
            </div>
          </div>
          <div class="cbox-iouter">
            <div class="cbox-item" @click="fnCCheck(9)">
              <div class="cbox-i" :class="[{ on: nCurrent === 9 && bOn }]">
                <div class="cbox-txt">台北<span>房市</span></div>
                <div class="cbox-n">9</div>
                <div class="cbox-p">
                  <span>
                    新店捷運站200公尺，散步3分鐘出站就到家，置產自住投資鞏固大台北房市基本盤
                  </span>
                </div>
              </div>
            </div>
          </div>
          <div class="cbox-iouter">
            <div class="cbox-item" @click="fnCCheck(10)">
              <div class="cbox-i" :class="[{ on: nCurrent === 10 && bOn }]">
                <div class="cbox-txt">渡假<span>飯店</span></div>
                <div class="cbox-n">10</div>
                <div class="cbox-p">
                  <span>
                    引入渡假飯店Resort設計，打造層峰專屬渡假休閒會館，雙門廳設計，KTV、宴會廳、美式運動Bar…寵愛名流社交生活
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="wave">
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
@import "src/assets/style/myvar"
#sec3
  position: relative

@media screen and (min-width: $bp-pc)
  .wave
    svg
      transform: translateX(-80vw)
  .sec3-imgbox
    // height: 70vw
    // background:
    //   image: url("./S3/bg.jpg")
    //   size: cover
    img
      width: 100%

@media screen and (max-width: $bp-mb)
  .wave
    svg
      transform: translateX(-20vw)
      // transform: rotateY(-180deg)
  .sec3-imgbox
    // height: 70vh
    background:
      image: url("./S3/bgm.jpg")
      size: cover
      position: 0 100%

  // #sec3-wt
//   height: 200px
//   margin-bottom: 200px
//   .wave
//     top: 0
</style>

<style lang="sass" scoped>
@import "src/assets/style/myvar"
@import src/assets/style/bbbS2Circle.sass

%center
  position: absolute
  left: 50%
  top: 50%
  transform: translate(-50%, -50%)

.cbox
  position: absolute
  user-select: none

.cbox-box
  width: $cw
  height: $cw
  position: relative
  &:before, &:after
    @extend %center
    content: ""
    border: solid 1px #fff
    border-radius: 50%
    opacity: .7

.cbox-iouter
  position: absolute
  width: 100%
  height: 100%
  transition: .3s
  cursor: pointer
  user-select: none

.cbox-item
  @extend %center
  z-index: 1
  transition: .3s
  transform: translate(-50% , calc(#{$cw}/2 - 50%))

.cbox-i
  position: relative
  display: flex
  justify-content: flex-start
  align-content: center
  flex-direction: column
  background: #fff
  border-radius: 50%
  padding: 20px
  box-shadow: 0 0 3px rgba(0,0,0,.5),0 0 3px rgba(0,0,0,.5)
  line-height: 1.5

.cbox-txt
  display: flex
  justify-content: center
  align-content: center
  flex-direction: column

$nw: 20px
.cbox-n
  transition: .3s
  position: absolute
  top: 5px
  left: 5px
  font-size: 12px
  display: flex
  align-items: center
  justify-content: center
  width: $nw
  height: $nw
  background: #fff
  border-radius: 50%
  box-shadow: 0 0 3px rgba(0,0,0,.5),0 0 3px rgba(0,0,0,.5)

.cbox-p
  display: none
  font-size: 12px
  span
    display: block
    height: 0
    transform: .7s
    overflow: hidden

//----
.cbox-i.on
  .cbox-p
    display: block
    position: relative
    span
      height: 70px
    &:after
      content: ""
      position: absolute
      width: 40%
      height: 2px
      background-color: #d1b373
      left: 50%
      transform: translateX(-50%)
      bottom: -20px

@media screen and (min-width: $bp-pc)
  $beforeW: 80%
  $afterW: 140%
  $iw: 120px
  .cbox-box
    width: $cw
    height: $cw
    &:before
      width: $beforeW
      height: $beforeW
    &:after
      width: $afterW
      height: $afterW

  .cbox-i
    font-size: 24px
    height: $iw
    width: $iw
    transition: .3s
  //----
  $iwon: 240px
  .cbox-i.on
    width: $iwon
    height: $iwon
    .cbox-txt
      margin-bottom: 12px
    .cbox-n
      top: -10px
      left: 50%
      transform: translateX(-50%)

  .cbox
    right: $cw / -3
    top: $cw / -3
@media screen and (max-width: $bp-mb)
  $beforeW: 600%
  $afterW: 950%
  $iw: 90px
  .cbox-box
    width: $cwm
    height: $cwm
    &:before
      width: $beforeW
      height: $beforeW
    &:after
      width: $afterW
      height: $afterW

  //----
  $iwon: 240px
  .cbox-i.on
    top: -300px
    width: $iwon
    height: $iwon
    .cbox-txt
      font-size: 24px
      margin-bottom: 12px
    .cbox-n
      top: -10px
      left: 50%
      transform: translateX(-50%)
  .cbox-i
    font-size: 16px
    height: $iw
    width: $iw
    transition: width .3s

  .cbox
    left: 50%
    transform: translateX(-50%)
    top: -40px
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
      nCurrent: 1,
      bOn: false
    }
  },

  methods: {
    fnCCheck(i) {
      if (i === this.nCurrent) {
        this.bOn = !this.bOn
      } else {
        this.nCurrent = i
      }
    }
  },

  created() {},

  mounted() {},

  computed: {}
}
</script>
