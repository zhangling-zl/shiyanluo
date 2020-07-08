<template>
  <div>
    <div class="featur j-center">
      <div class="featur-center">
        <div>
          <div v-for="(item,index) in img1.slice(0,1) " :key="index" class="j-flex j-between">
            <img :src="item.recommend_course.picture_url" alt class="img11" />
            <div v-for="(item1,index1) in item.courses.slice(0,2)" :key="index1">
              <div class="from">
                <img :src="item1.picture_url" class="img22" />
              </div>
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
  .featur-center {
    width: 1140px;
  }
}
.img11 {
  width: 550px;
  height: 250px;
}
.img22 {
  width: 260px;
  height: 150px;
}
.from{
  width: 260px;
  height: 250px;
  background-color: #fff;
}
</style>