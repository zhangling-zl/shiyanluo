<template>
  <div>
    <div v-for="(item,index) in img1.slice(1,2)" :key="index">
      <div v-for="(item1,index1) in item.courses.slice(8,12)" :key="index1">
      <img :src="item1.picture_url" alt="">
      
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
    return {
      courses: []
    };
  },
  methods: {},
  mounted() {},
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
</style>