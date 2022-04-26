<template>
  <div class="cbox">
    <div class="cbox-box">
      <div class="cbox-iouter current">
        <div class="cbox-i">多角<span>視野</span></div>
      </div>
      <div class="cbox-iouter">
        <div class="cbox-i">絕版<span>地王</span></div>
      </div>
      <div class="cbox-iouter">
        <div class="cbox-i">國際<span>地標</span></div>
      </div>
      <div class="cbox-iouter">
        <div class="cbox-i">山水<span>版圖</span></div>
      </div>
      <div class="cbox-iouter">
        <div class="cbox-i">換屋<span>首選</span></div>
      </div>
      <div class="cbox-iouter">
        <div class="cbox-i">食衣<span>住行</span></div>
      </div>
      <div class="cbox-iouter">
        <div class="cbox-i">首席<span>設計</span></div>
      </div>
      <div class="cbox-iouter">
        <div class="cbox-i">SRC<span>鋼骨</span></div>
      </div>
      <div class="cbox-iouter">
        <div class="cbox-i">台北<span>房市</span></div>
      </div>
      <div class="cbox-iouter">
        <div class="cbox-i">渡假<span>飯店</span></div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="sass" scoped>
@import "src/assets/style/myvar"
@import src/assets/style/bbbS2Circle.sass
$iw: 100px
$afterW: 70%
%center
  position: absolute
  left: 50%
  top: 50%
  transform: translate(-50%, -50%)
.cbox
  @extend %center

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
  &:before
    width: 100%
    height: 100%
  &:after
    width: $afterW
    height: $afterW

.cbox-iouter
  position: absolute
  width: 100%
  height: 100%
  transition: .3s
  cursor: pointer
  user-select: none

.cbox-i
  @extend %center
  display: flex
  flex-direction: column
  background: #fff
  border-radius: 50%
  padding: 20px
  box-shadow: 0 0 3px rgba(0,0,0,.5),0 0 3px rgba(0,0,0,.5)
  line-height: 1.5
  font-size: 18px
  height: $iw
  width: $iw
  z-index: 1
  transition: .3s
  // transform-origin: 50% 0
  transform: translate(-50% , calc(#{$cw}/2 - 50%))
  &:nth-child(1)
    // transform: translate(-50% , calc(#{$cw}/2 - 50%)) rotate(36deg)
  //   transform-origin: 50% 50%
  //   transform-origin: 0
  //   transform-origin: 100%
</style>
