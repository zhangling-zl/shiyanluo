<template>
  <div>
    <div class="featur j-center">
      <div class="featur-center">
        <div v-for="(item,index) in img1.slice(0,1) " :key="index">
          <img :src="item.recommend_course.picture_url" alt="">
          <div v-for="(item1,index1) in item.courses" :key="index1">
            <img :src="item1.picture_url" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {
    img1: {
      type: Array
    }
  },
  components: {},
  data() {
    return {};
  },
  methods: {},
  mounted() {},
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.featur {
  background-color: rgb(249, 249, 249);
  .featur-center{
    width: 1140px;
  }
}

</style>