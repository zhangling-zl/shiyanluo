<template>
  <div>
  x小可爱
    <div v-for="(item,index) in attend" :key="index">
      <img :src="item.picture_url" alt />
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {
    attend: {
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
</style>