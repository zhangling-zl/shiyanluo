<template>
  <div>
    <div class="boxs j-center">
      <div class="boxs-center j-between">
        <div v-for="(item) in paths" :key="item">
          <div class="from">
            <img :src="item.image" alt />
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
.from{
    width: 250px;
    height: 260px;
    background-color: #fff;
    margin-bottom: 40px;
}
</style>