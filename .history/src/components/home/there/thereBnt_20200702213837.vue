<template>
  <div>
    <div class="thereBnt j-center">
      <div class="thereBnt-center j-flex">
        <div v-for="(item,index) in attend" :key="index">
        
          <img :src="item.picture_url" alt />
          <div>{{item.title}}</div>
        </div>
      </div>
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
.thereBnt {
  background-color: rgb(249, 249, 249);
  .thereBnt-center{
   width: 75%;
  }
}
</style>