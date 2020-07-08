<template>
  <div>
    <div class="frame j-center">
      <div class="frame-center">
        <swiper ref="mySwiper" :options="swiperOptions">
          <swiper-slide>Slide 1</swiper-slide>
         
          <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
      </div>
    </div>
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
  components: {},
  data() {
    return {
      swiperOptions:{}//轮播图的配置选项
    };
  },
  methods: {},
  mounted() {},
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.frame {
  width: 100%;
  height: 100%;
  background-color: rgb(249, 249, 249);
  box-shadow: 1px -1px 14px #eee;
}
.frame-center {
  width: 1140px;
}
</style>