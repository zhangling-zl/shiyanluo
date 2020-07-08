<template>
  <div>
    <div class="featur j-center">
      <div class="featur-center">
        <div v-for="(item,index) in img1.slice(0,1) " :key="index">
          <img :src="item.recommend_course.picture_url" alt />
          <div v-for="(item1,index1) in item.courses.slice(0,2)" :key="index1">
            <img :src="item1.picture_url" alt />
            <div>{{item1.name}}</div>
            <div class="j-flex al-cnter"> 
              <i class="iconfont icon-jiaoyin jiaoyin m-r-5"></i>
              <div class="text1 f-14">{{item1.students_count}}</div>
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
.jiaoyin {
  font-size: 14px !important;
  color: rgb(155, 157, 162);
}
.text1{
   color: rgb(155, 157, 162);
}
</style>