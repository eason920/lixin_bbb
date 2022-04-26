<template>
  <div class="contact" id="contact">
    <div class="wave up">
      <!-- <img src="./S6/wwave.svg" /> -->
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
    <Order />
    <HouseInfo />
  </div>
</template>
<style lang="sass" scoped>
@import "src/assets/style/myvar"
#contact
  background: #fff
@media screen and (min-width: $bp-pc)
  #contact
    padding-top: 200px

@media screen and (max-width: $bp-mb)
  #contact
    padding-top: 80px
</style>

<script>
import Order from '@/components/Order.vue'
import HouseInfo from '@/components/HouseInfo.vue'

export default {
  name: 'contactSection',
  components: {
    Order,
    HouseInfo
  },

  methods: {}
}
</script>
