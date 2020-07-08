<template>
  <div>
    <div class="boxs j-center">
      <div class="boxs-center j-between">
        <div v-for="(item) in paths" :key="item">
        <img :src="item.image" alt=""></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {
    paths: {
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
.boxs {
  background-color: rgb(249, 249, 249);
  .boxs-center {
    width: 1140px;
    flex-wrap: wrap;
  }
}
</style>