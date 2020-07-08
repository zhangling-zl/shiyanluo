<template>
  <div>
    <!--导航栏-->
    <navHome></navHome>
    <!--banner广告图-->
    <bannerHome :banner="banner" v-if="banner.length>0"></bannerHome>
    <!--楼+ 实战课程-->
    <thereTop title1="楼+ 实战课程" title2="定期开班，导师助教全程辅导，最快最优成长"></thereTop>
    <thereBnt :attend="attend" v-if="attend.length>0"></thereBnt>
    <!--精选项目课-->
    <featuredTop>
      <template v-slot:text1>
        <div v-if="img1.length>0">{{img1[0].classify_name}}</div>
      </template>
      <template v-slot:text2>
        <div v-if="img1.length>0">{{img1[0].description}}</div>
      </template>
    </featuredTop>
    <featuredBnt :img1="img1" v-if="img1.length>0"></featuredBnt>
    <!--近期好课-->
    <goodclassTop>
      <template v-slot:text3>
        <div v-if="img1.length>0">{{img1[1].classify_name}}</div>
      </template>
      <template v-slot:text4>
        <div v-if="img1.length>0">{{img1[1].description}}</div>
      </template>
    </goodclassTop>
    <goodclassBnt :img1='img1' v-if="img1.length>0">></goodclassBnt>
  </div>
</template>

<script>
import navHome from "../components/home/navHome";
import bannerHome from "../components/home/bannerHome";
import thereTop from "../components/home/there/thereTop";
import thereBnt from "../components/home/there/thereBnt";

import featuredTop from "../components/home/four/featuredTop";
import featuredBnt from "../components/home/four/featuredBnt";

import goodclassTop from "../components/home/fivr/goodclassTop";
import goodclassBnt from "../components/home/fivr/goodclassBnt";

import axios from "axios";
export default {
  name: "",
  props: {},
  components: {
    navHome,
    bannerHome,
    thereTop,
    thereBnt,
    featuredTop,
    featuredBnt,
    goodclassTop,
    goodclassBnt
  },
  data() {
    return {
      banner: [],
      attend: [], //实验课程
      img1: []
    };
  },
  methods: {
    //轮播图请求
    getData() {
      axios
        .get("http://120.78.14.107/api/v2/index/banner-pictures")
        .then(res => {
          if (res.data.length > 0) {
            this.banner = res.data;
          }
        })
        .catch(err => {
          console.log(err);
        });
    },
    //楼+实战课程请求
    getData1() {
      axios
        .get("http://120.78.14.107/api/v2/index/louplus")
        .then(res => {
          if (res.data.length > 0) {
            this.attend = res.data;
          }
          console.log(res.data);
        })
        .catch(err => {
          console.log(err);
        });
    },
    //课程分类
    getData2() {
      axios
        .get("http://120.78.14.107/api/v2/index/classfication-courses")
        .then(res => {
          if (res.data.length > 0) {
            this.img1 = res.data;
            console.log(res.data);
          }
        })
        .catch(err => {});
    }
  },
  mounted() {
    this.getData(), this.getData1();
    this.getData2();
  },
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
* {
  margin: 0;
  padding: 0;
}
</style>