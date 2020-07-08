<template>
  <div>
    <div class="boxs j-center">
      <div class="boxs-center">
       <div v-for="(item,index) in strengthen" :key="index">
       <img :src="item.picture_url" class="img"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {
    strengthen: {
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
.img{
  width: 455px;
  height: 250px;
}
</style>