<template>
  <div class="menu" :class="[{ isWhite: bIsWhite }]">
    <ul>
      <li
        :key="item.name"
        v-scroll-to="{
          element: `#${item.section}`,
          offset: item.offset ? item.offset : offset
        }"
        v-for="item in list"
      >
        <a href="#" @click.prevent="">{{ item.name }}</a>
      </li>

      <!-- <li
        :key="item.name"
        v-scroll-to="{
          element: `#${item.section}`,
          offset: item.offset ? item.offset : offset
        }"
        v-for="item in list"
        class="flex-ac"
        @click="toggleSidebar"
      ></li> -->
    </ul>
  </div>
</template>

<script>
import $ from 'jquery'
import { isMobile, isTablet } from '@/utils'
import navList from '@/info/navList'

export default {
  name: 'navigation',
  components: {},
  data() {
    return {
      isOpen: false,
      isMobile,
      isTablet,
      list: navList,
      bIsWhite: false
    }
  },

  computed: {
    offset() {
      if (this.isMobile) {
        return -39
      }

      if (this.isTablet) {
        return -45
      }

      return -56
    }
  },

  mounted() {
    if (!isMobile) {
      if ($(window).scrollTop() > 200) {
        this.bIsWhite = true
      }
      $(window).scroll(() => {
        this.bIsWhite = $(window).scrollTop() > 200
      })
    }
  }
}
</script>

<style lang="sass" scoped>
// nav
$gray: #333
.menu
  position: fixed
  top: 0
  left: 0
  display: flex
  z-index: 9999
  width: 100%
  align-items: center
  justify-content: center
  transition: background .3s
  ul
    display: flex
    align-items: center
    width: 60vw
  li
    width: calc( 100% / 6 )
  a
    display: block
    padding: 30px 0
    font-size: 1.3vw
    text-decoration: none
    color: #fff
    letter-spacing: .1vw
    position: relative
    transition: color .3s
    &:after
      content: ""
      position: absolute
      bottom: 0
      left: 0
      display: block
      width: 100%
      height: 2px
      background-color: #fff
      opacity: .6
      transform: scaleX(0)
      transition: transform .4s ease
      transform-origin: 0% 50%
    &:hover:after
      transform: scaleX(1)
  // white
  &.isWhite
    background-color: #fff
    a
      color: $gray
      &:after
        background-color: $gray
</style>
