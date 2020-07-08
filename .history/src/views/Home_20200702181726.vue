<template>
  <div>
    <navHome></navHome>
    <bannerHome :banner='banner'></bannerHome>
    <thereTop :title1="楼+实战课程" :title2=" 定期开班，导师助教全程辅导，最快最优成长"></thereTop>
    <thereBnt></thereBnt>
    
  </div>
</template>

<script>
import navHome from "../components/home/navHome";
import bannerHome from "../components/home/bannerHome";
import thereTop from '../components/home/there/thereTop'
import thereBnt from '../components/home/there/thereBnt'
import axios from "axios";
export default {
  name: "",
  props: {},
  components: {
    navHome,
    bannerHome,
    thereTop,
    thereBnt

 
  },
  data() {
    return {
      banner:[]
    };
  },
  methods: {
    getData() {
      axios
        .get("http://120.78.14.107/api/v2/index/banner-pictures")
        .then(res => {
          if(res.data.length>0){
          this.banner=res.data
          }
          console.log(res.data);

        })
        .catch(err => {
          console.log(err);
        });
    }
  },
  mounted() {
    this. getData()
  },
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
*{
  margin: 0;
  padding: 0;
}
</style>