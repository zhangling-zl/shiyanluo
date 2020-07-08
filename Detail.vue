<template>
  <div class="box">
    <swiper ref="mySwiper" :options="swiperOptions" class="swiper" v-if="swipers.length">
      <swiper-slide v-for="(item, index) in swipers" :key="index" class="item">
        <div :style="{background: item.background_color}" class="con"></div>
        <div class="img">
          <img :src="item.picture_url" alt />
        </div>
        <div :style="{background: item.background_color}" class="con"></div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
      <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div>
    </swiper>
  </div>
</template>

<script>
import axios from 'axios'
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
export default {
  name: '',
  props: {
  },
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      swipers: [],
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
        // 是否循环播放
        loop: true,
        autoplay: true
      }
    }
  },
  methods: {
    getData() {
      axios.get('http://120.78.14.107/api/v2/index/banner-pictures').then(res => {
        if (res.data.length > 0) {
          this.swipers = res.data
        }
        console.log(res.data)
      }).catch(err => {
        console.log(err)
      })
    },
    pre() {
      console.log(this.$refs.mySwiper)
    },
    next() {

    }
  },
  mounted() {
    this.getData()
    // window.addEventListener('scroll', () => {
    //   let top = document.documentElement.scrollTop
    //   console.log(top)
    // })
  },
  watch: {

  },
  computed: {

  }
}
</script>

<style scoped lang='scss'>
.box {
  height: 515px;
  .swiper {
    height: 515px;
    position: relative;
    --swiper-navigation-size: 20px;
    .item {
      display: flex;
      .img {
        width: 1170px;
        img {
          width: 100%;
          height: 100%;
        }
      }
    }
    .con {
      flex: 1;
      height: 515px;
    }
  }
}
.swiper-button-prev {
  position: absolute;
  left: 35%;
  color: #fff;
}
.swiper-button-next {
  position: absolute;
  color: #fff;
  right: 19%;
}
</style>