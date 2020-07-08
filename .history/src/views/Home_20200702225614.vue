<template>
  <div>
    <navHome></navHome>
    <bannerHome :banner="banner"></bannerHome>

    <thereTop title1="楼+ 实战课程" title2="定期开班，导师助教全程辅导，最快最优成长"></thereTop>
    <thereBnt :attend="attend"></thereBnt>

    <featuredTop>
      <template v-slot:text1>
        <div v-if="arr.length>0">{{arr[0].classify_name}}</div>
      </template>
      <template v-slot:text2>
        <div v-if="arr.length>0">{{arr[0].description}}</div>
      </template>
    </featuredTop>
    <featuredBnt :arr='arr'></featuredBnt>
  </div>
</template>

<script>
import navHome from "../components/home/navHome";
import bannerHome from "../components/home/bannerHome";
import thereTop from "../components/home/there/thereTop";
import thereBnt from "../components/home/there/thereBnt";

import featuredTop from "../components/home/four/featuredTop";
import featuredBnt from "../components/home/four/featuredBnt";

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
    featuredBnt
  },
  data() {
    return {
      banner: [],
      attend: [], //实验课程
      arr: []
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
            this.arr= res.data;
             console.log(res.data);
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