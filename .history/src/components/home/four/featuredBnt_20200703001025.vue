<template>
  <div>
    <div class="featur j-center">
      <div class="featur-center">
        <div v-for="(item,index) in img1.slice(0,1) " :key="index" class="j-flex j-between">
          <img :src="item.recommend_course.picture_url" alt class="img11" />
          <div v-for="(item1,index1) in item.courses.slice(0,2)" :key="index1">
            <div class="z-c-text">
              <img :src="item1.picture_url" alt class="img22" />
              <div class="p-10">
                <div>{{item1.name}}</div>
                <div class="j-between al-cnter m-t-20">
                  <div class="j-flex al-cnter">
                    <i class="iconfont icon-jiaoyin jiaoyin m-r-5"></i>
                    <div class="text1 f-12">{{item1.students_count}}</div>
                  </div>
                  <div class="z-c-text3 f-12 j-center al-cnter" v-if="item1.fee_type===bootcamp">训练营</div>
                </div>
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
.z-c-text {
  background-color: #fff;
  box-shadow: 1px 1px 1px #ccc;
  flex-wrap: wrap;
  &:hover {
    box-shadow: 1px 1px 20px #ccc;
  }
}
.jiaoyin {
  font-size: 14px !important;
  color: rgb(155, 157, 162);
}
.text1 {
  color: rgb(155, 157, 162);
}
.img11 {
  width: 550px;
  box-shadow: 1px 1px 1px #ccc;
  &:hover {
    box-shadow: 1px 1px 20px #ccc;
  }
}
.img22 {
  width: 255px;
  height: 150px;
}
.z-c-text3 {
  width: 60px;
  height: 20px;
  background-color: rgb(255, 102, 102);
  border-radius: 15px;
  color: #fff;
}
</style>