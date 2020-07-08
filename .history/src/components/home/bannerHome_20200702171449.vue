<template>
  <div>
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="(item,index) in banner" :key="index">
        <div class="j-flex picture">
          <div class="left" :style="{background:item.background_color}"></div>
          <img :src="item.picture_url" alt class="img" />
          <div class="left" :style="{background:item.background_color}"></div>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
      <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";
export default {
  name: "",
  props: {
    banner: {
      type: Array
    }
  },
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      //轮播图的配置选项
      swiperOptions: {
        //下面的分页效果
        pagination: {
          el: ".swiper-pagination",
          clickable: true
        },
        loop: true, //是否循环播放
        autoplay: true, //自动播放
        observer: true,
        //左右箭头
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        }
      }
    };
  },
  methods: {},
  mounted() {},
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.left {
  width: 30%;
}
.picture.img{
  width: 70%;
}
.swiper-button-prev{
  left: 460px;
 
  color: #ccc;
}
.swiper-button-next{
  right: 210px;
   color: #ccc;
}
</style>