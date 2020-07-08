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
                <div class="text j-between al-cnter">
                  <div class="j-flex al-cnter">
                    <i class="iconfont icon-jiaoyin jiaoyin m-r-5"></i>
                    <div class="text1 f-12">{{item1.id}}</div>
                  </div>
                  <div class="text2 j-center al-cnter f-12">训练营</div>
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
.img11 {
  width: 550px;
  height: 250px;
  margin-bottom: 60px;
}
.img22 {
  width: 260px;
  height: 150px;
}
.from {
  width: 260px;
  height: 250px;
  background-color: #fff;
}

.jiaoyin {
  font-size: 14px !important;
  color: rgb(155, 157, 162);
}
.text1 {
  color: rgb(155, 157, 162);
}
.text2 {
  width: 50px;
  height: 20px;
  background-color: rgb(255, 102, 102);
  border-radius: 15px;
  color: #fff;
}
.text{
  width: 260px;
  height: 50px;
  background-color:#ccc;
}
</style>