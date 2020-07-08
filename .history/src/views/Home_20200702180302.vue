<template>
  <div>
    <navHome></navHome>
    <bannerHome :banner='banner'></bannerHome>
    
  </div>
</template>

<script>
import navHome from "../components/home/navHome";
import bannerHome from "../components/home/bannerHome";
import axios from "axios";
export default {
  name: "",
  props: {},
  components: {
    navHome,
    bannerHome
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