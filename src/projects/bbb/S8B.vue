<template>
  <div class="relative">
    <section id="s8b">
      <div class="s8bt" data-aos="fade-up" data-aos-duration="800">
        <span>涵碧美學御所</span>
        <p>人生必修的一堂OFF學</p>
      </div>
      <div class="s8bb">
        <p data-aos="fade-up" data-aos-duration="800">
          ON(工作)&OFF(休閒)兩大學問，你修了多少學分？事業成功、家庭圓滿、生活精彩，才是真正的成功人生！因應回家社交、回家休閒趨勢，除了居住，更要享受，進門就像在Villa度假，「碧波白」重新發現「家」的奧妙，讓OFF成為永不褪流行的潮流。
        </p>
        <div class="bblock" data-aos="fade-up" data-aos-duration="800"></div>
      </div>
    </section>
  </div>
</template>

<style lang="sass" scoped>
@import "~@/assets/style/myvar"
#s8b
  background: #f2f2f2
  padding: 0 5vw 5vw
  letter-spacing: 1px
  color: #000
.s8bt
  display: flex
  flex-direction: column
  align-items: flex-end
  padding-bottom: 5px
  margin-bottom: 20px
  span
    font-size: 40px
    display: block
    padding-bottom: 20px
  p
    font-size: 32px
    position: relative

.s8bb
  display: flex
  p
    text-align: left
    font-size: 16px
    line-height: 2.5

@media screen and (min-width: $bp-pc)
  .s8bt
    border-bottom: solid 1px #000
    p
      &:after
        content: ""
        position: absolute
        height: 5px
        width: 110%
        bottom: -8px
        right: 0
        background: #f2f2f2

  .s8bb
    justify-content: space-between
    align-items: flex-end
    p
      width: 50%
@media screen and (max-width: $bp-mb)
  #s8b
    padding-bottom: 10vh
  .s8bt
    padding-bottom: 25px
    margin-bottom: 0
    position: relative
    &:before
      content: ""
      position: absolute
      left: 0
      top: 10px
      height: 1px
      width: 100%
      background: #666

    span
      font-size: 20px
      padding-bottom: 10px
      background-color: #f2f2f2
      position: relative
      z-index: 1
      padding-left: 10px
    p
      font-size: 24px

  .s8bb
    flex-direction: column
    align-items: flex-end
    p
      font-size: 16px
      line-height: 2.5
      padding-bottom: 20px
</style>
