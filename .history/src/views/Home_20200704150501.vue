<template>
  <div>
    <!--导航栏-->
    <navHome></navHome>
    <!--banner广告图-->
    <bannerHome :banner="banner" v-if="banner.length>0"></bannerHome>
    <!--楼+ 实战课程-->
    <thereTop title1="楼+ 实战课程 |" title2="定期开班，导师助教全程辅导，最快最优成长"></thereTop>
    <thereBnt :attend="attend" v-if="attend.length>0"></thereBnt>

    <!-- 精选项目课
     <featuredTop>
      <template v-slot:text1>
        <div v-if="img1.length>0">{{img1[0].classify_name}}</div>
      </template>
      <template v-slot:text2>
        <div v-if="img1.length>0">{{img1[0].description}}</div>
      </template>
    </featuredTop>
    <featuredBnt :img1="img1" v-if="img1.length>0"></featuredBnt>
   近期好课
    <goodclassTop>
      <template v-slot:text3>
        <div v-if="img1.length>0">{{img1[1].classify_name}}</div>
      </template>
      <template v-slot:text4>
        <div v-if="img1.length>0">{{img1[1].description}}</div>
      </template>
    </goodclassTop>
    <goodclassBnt :img1="img1" v-if="img1.length>0">></goodclassBnt>
    基本功
    <basicskillTop>
      <template v-slot:text5>
        <div v-if="img1.length>0">{{img1[2].classify_name}}</div>
      </template>
      <template v-slot:text6>
        <div v-if="img1.length>0">{{img1[2].description}}</div>
      </template>
    </basicskillTop>
    <basicskillBnt :img1="img1" v-if="img1.length>0"></basicskillBnt>
    后端开发
    <rearendTop>
      <template v-slot:text7>
        <div v-if="img1.length>0">{{img1[3].classify_name}}</div>
      </template>
    </rearendTop>
    <rearendBnt></rearendBnt>-->

    <buildingTitle>
      <template #big>精选项目课 |</template>
      <template #small>精选会员项目课程，动手中收获</template>
      <template #more>更多>></template>
    </buildingTitle>
    <courseSorts :Sorts='Sorts[0]' v-if="Sorts.length>0"></courseSorts>
    <!-- 标题 -->

    <buildingTitle>
      <template #big>近期好课 |</template>
      <template #small>及时学习，跟进时代的脚步</template>
      <template #more>更多>></template>
    </buildingTitle>
    <courseSorts :Sorts="Sorts[1] " v-if="Sorts.length>0"></courseSorts>

    <buildingTitle>
      <template #big>基本功 |</template>
      <template #small>行业专家打造的免费基础课程，注册即可学习</template>
      <template #more>更多>></template>
    </buildingTitle>
    <courseSorts :Sorts="Sorts[2] " v-if="Sorts.length>0"></courseSorts>

    <buildingTitle>
      <template #big>后端开发 </template>
      <template #small></template>
      <template #more>更多></template>
    </buildingTitle>
    <computing :Sorts='Sorts[3]' v-if="Sorts.length>0"></computing>

    <buildingTitle>
      <template #big>云计算与人工智能 </template>
      <template #small></template>
      <template #more>更多></template>
    </buildingTitle>
    <computing :Sorts='Sorts[4]' v-if="Sorts.length>0"></computing>
    
  </div>
</template>

<script>
import navHome from "../components/home/navHome";
import bannerHome from "../components/home/bannerHome";
import thereTop from "../components/home/there/thereTop";
import thereBnt from "../components/home/there/thereBnt";


import buildingTitle from "../components/home/buildingTitle"; //标题
import courseSorts from '../components/home/courseSorts'//课程分类
import computing from '../components/home/computing'//云计算

import axios from "axios";
export default {
  name: "",
  props: {},
  components: {
    navHome,
    bannerHome,
    thereTop,
    thereBnt,
   
    buildingTitle, //标题
    courseSorts,//课程分类
    computing,//云计算
  },
  data() {
    return {
      banner: [],//轮播图
      attend: [], //实验课程
      // img1: [],
      Sorts:[],//课程分类
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
            this.Sorts = res.data;
            console.log(res.data);
          }
        })
        .catch(err => {});
    },
    //训练营强化
    getData3() {
      axios
        .get("http://120.78.14.107/api/v2/index/bootcamps/")
        .then(res => {
          if (res.data.length > 0) {
            // this.Sorts = res.data;
            console.log(res.data);
          }
        })
        .catch(err => {});
    }
  },
  mounted() {
    this.getData(), this.getData1();
    this.getData2();
    this.getData3();
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