<template>
  <div>
    <navHome></navHome>
    <bannerHome></bannerHome>
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
    return {};
  },
  methods: {
    getData() {
      axios
        .get("http://120.78.14.107/api/v2/index/banner-pictures")
        .then(res => {
          console.log(res.data);
        })
        .catch(err => {
          console.log(err);
        });
    }
  },
  mounted() {},
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
</style>