<template>
  <div>
    <div class="banner">
      <div class="fication">
        <div v-for="(item,index) in course" :key="index">
          <div class="from1 j-center al-cnter">
            <div class="text-one fff">{{item.name}}</div>
            <div class="text-tow fff f-14">{{item.tags[0].name}}</div>
            <div class="text-there fff f-14">{{item.tags[1].name}}</div>
          </div>
        </div>
      </div>

      <swiper ref="mySwiper" :options="swiperOptions">
        <swiper-slide v-for="(item,index) in banner" :key="index">
          <div class="left" :style="{background:item.background_color}">
            <img :src="item.picture_url" alt class="imgs" />
          </div>
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
        <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
      </swiper>
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
    },
    course: {
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
  display: flex;
  width: 100%;
  height: 552px;
  position: relative;
}
.imgs {
  width: 1140px;
  height: 552px;
  position: absolute;
  left: 190px;
}
.swiper-button-prev {
  left: 460px;
  color: rgb(172, 170, 161);
}
.swiper-button-next {
  right: 160px;
  color: rgb(245, 245, 245);
}
.fication {
  width: 260px;
  background-color: rgba(0, 0, 0, 0.2);
  position: absolute;
  height: 552px;
  left: 189.5px;
  z-index: 99;
}
.banner {
  position: relative;
}
.from1{
  width: 260px;
  height: 50px;
}
</style>