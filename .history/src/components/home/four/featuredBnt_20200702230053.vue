<template>
  <div>
    <div class="featur j-center">
      <div class="featur-center">
      我是小可爱
        <div v-for="(item,index) in arr.slice(0,1) " :key="index">
          <img :src="item.recommend_course.picture_url" alt />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {
    arr: {
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
  .featur{
    width: 75%;
  }
}
</style>