<template>
  <div>
    <div class="thereBnt j-center">
      <div class="thereBnt-center j-between">
        <div v-for="(item,index) in attend.slice(0,4)" :key="index">
          <div class="item">
            <img :src="item.picture_url" alt />
            <div class="text m-10">
              <div class="text1">{{item.title}}</div>
              <div class="text2 f-14 m-t-10 ">最近班次:{{item.open_time}}</div>
            </div>
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
  .thereBnt-center {
    width: 75%;
  }
}

img {
  border-radius: 10px 10px 0 0;
  width: 260px;
  height: 90px;
}
.item {
  border-radius: 10px 10px 10px 10px;
 box-shadow: 1px 1px 8px #ccc;
}
.text1 {
  color: rgb(86, 86, 86);
}
.text2 {
  color: rgb(164, 164, 164);
}

</style>