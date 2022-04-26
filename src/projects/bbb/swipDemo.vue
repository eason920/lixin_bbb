<template>
  <div class="section3">
    <div
      class="swipe absolute"
      @mouseenter.stop="toggleTimer = false"
      @mouseleave.stop="toggleTimer = true"
    >
      <div
        class="swipe-wrap relative"
        v-touch:swipe.left="decIndex"
        v-touch:swipe.right="addIndex"
      >
        <img
          v-for="(slide, i) in slideList"
          :src="slide.img"
          :key="slide.img"
          alt="城南豐穰"
          :class="
            `swipe-item absolute ${slideIndex === i ? 'active' : ''} ${
              slideIndex === i + 1 || slideIndex === i - slideList.length + 1
                ? 'base'
                : ''
            }`
          "
        />
        <div class="pagination absolute flex-ac">
          <div
            :class="`pagination-dot`"
            v-for="(slide, index) in slideList"
            :key="slide.img + '-dot'"
            @click="goTo(index)"
          >
            <span :class="`${slideIndex === index ? 'active' : ''}`"></span>
          </div>
        </div>
        <div class="swipe-btns absolute flex-ac flex-jb">
          <img
            src="./all/prev-btn.png"
            alt=""
            class="prev-btn"
            @click="decIndex"
          />
          <img
            src="./all/next-btn.png"
            alt=""
            class="next-btn"
            @click="addIndex"
          />
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.divider {
  bottom: 0;
}
.Masthead {
  overflow: visible !important;
  z-index: 1 !important;
}
.swipe-wrap {
  width: 100%;
  height: 100%;
  overflow: hidden;
  font-size: 1.04vw;
}
.swipe-item {
  width: 100%;
  height: 100%;
  left: 100%;
  transition: left 1s ease-in-out;
  z-index: 0;
  &.base {
    z-index: 1;
    left: 0;
  }
  &.active {
    z-index: 2;
    left: 0;
  }
}
.pagination {
  width: auto;
  bottom: 2em;
  left: 0;
  right: 0;
  margin: 0 auto;
  justify-content: center;
}
.pagination-dot {
  padding: 0 0.5em;
  cursor: pointer;
  z-index: 4;
  span {
    display: block;
    width: 0.5em;
    height: 0.5em;
    border-radius: 1em;
    box-shadow: 0 0 0 1px #fff;
    position: relative;
    background-color: rgba(0, 0, 0, 0.01);
    transition: all 0.5s;
    &::before {
      content: '';
      width: 100%;
      height: 100%;
      display: block;
      background: #fff;
      border-radius: 50%;
      opacity: 1;
      position: absolute;
      top: 0%;
      left: 0%;
      transition: all 0.3s;
      transform-origin: center;
      transform: scale(0);
    }
    &.active {
      &::before {
        content: '';
        width: 100%;
        height: 100%;
        display: block;
        background: #fff;
        border-radius: 50%;
        opacity: 1;
        position: absolute;
        top: 0%;
        left: 0%;
        transform: scale(1);
      }
    }
  }
}
.swipe-btns {
  width: 100%;
  height: 100%;
  padding: 0 0.5em;
  z-index: 3;
  .prev-btn,
  .next-btn {
    width: 1em;
    cursor: pointer;
  }
}
@media screen and (max-width: 767px) {
  .swipe-wrap {
    font-size: 5.3333333333vw;
  }

  .pagination {
    bottom: 0.5em;
  }
  .pagination-dot {
    span {
      width: 0.5em;
      height: 0.5em;
    }
  }
  .swipe-btns {
    padding: 0 0.5em;
    .prev-btn,
    .next-btn {
      width: 0.5em;
    }
  }
}
</style>
<style lang="scss" scoped>
@import '@/assets/style/function.scss';
.section3 {
  width: 100vw;
  height: 42vw;
}

.title {
  top: size(160);
  left: size(180);
  font-size: size(30);
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.67;
  letter-spacing: normal;
  text-align: left;
  color: #976a4b;
  font-family: 'DFLiSongStd';
}
.desc {
  font-family: 'DFLiSongStd';
  width: size(442);
  top: size(330);
  left: size(182);
  font-size: size(21);
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 2.14;
  letter-spacing: normal;
  text-align: justify;
  color: #000000;
}
.swipe {
  width: size(1200);
  height: size(800);
  top: 0;
  right: 0;
  object-fit: cover;
}
@media only screen and (max-width: 1440px) {
}
@media only screen and (max-width: 1280px) and (min-width: 1025px) {
  .fullscreen {
    height: 100vh;
  }
}
/* 螢幕尺寸標準 */
/* 平板尺寸 */
@media only screen and (min-device-width: 768px) and (max-device-width: 1024px) {
}
@media screen and (max-width: 767px) {
  .section3 {
    width: 100vw;
    height: size-m(800);
  }
  .title {
    top: size-m(540);
    right: auto;
    left: size-m(110);
    font-size: size-m(20);
    text-align: center;
  }
  .desc {
    width: size-m(295);
    top: size-m(650);
    right: auto;
    left: size-m(41);
    font-size: size-m(15);
    line-height: 1.8;
    text-align: center;
  }
  .swipe {
    width: 100vw;
    height: calc(100vw / 0.75);
    top: 0;
    left: 0;
    object-fit: cover;
  }
}
</style>

<script>
// @ is an alias to /src
import { isMobile, isTablet } from '@/utils'
// import Parallax from 'vue-parallaxy'
import slider from '@/mixins/slider.js'

export default {
  name: 'sectiondSwip',

  mixins: [slider],

  // components: {
  //   Parallax,
  // },

  data() {
    return {
      isMobile,
      isTablet,
      slideList: isMobile
        ? [
          {
            img: require('./S9/38-1.jpg')
          },
          {
            img: require('./S9/38-2.jpg')
          },
          {
            img: require('./S9/38-3.jpg')
          }
        ]
        : [
          {
            img: require('./S9/45b-1.jpg')
          },
          {
            img: require('./S9/45b-2.jpg')
          },
          {
            img: require('./S9/45b-3.jpg')
          }
        ]
    }
  },

  methods: {},

  created() {},

  mounted() {},

  computed: {}
}
</script>
