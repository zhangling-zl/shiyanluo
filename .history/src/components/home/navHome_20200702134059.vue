<template>
  <div>
    <div class="frame j-center">
      <div class="frame-center">
        <div class="top j-between">
          <div class="left f-18 j-center al-cnter">
            <img src="../../assets/imgs/9f43b00.svg" alt="logo" />
            <div>做实验，学编程</div>
          </div>
          <div class="rigth j-center">
            <div class="j-center al-cnter text12">
              <div class="text1">企业版</div>
              <div class="line m-l-r-10"></div>
              <div class="text2">学校版</div>
            </div>
            <div class="text3 j-center al-cnter">登录</div>
            <div class="text4 j-center al-cnter">注册</div>
          </div>
        </div>
        <div class="buttom j-center">
          <div class="b-left al-cnter j-flex">
            <div class="j-flex m-l-20">
              <i class="iconfont icon-gengduo1 icon-All m-r-10"></i>
              <div class="b-text fff">全部课程</div>
            </div>
          </div>
          <div class="b-rigth">
            <div class="b-rigth-text al-cnter j-flex">
              <div class="b-r-text m-t-10 m-b-10 m-r-20">路径</div>
              <div class="b-r-text m-t-10 m-b-10 m-r-20">训练营</div>
              <div class="b-r-text m-t-10 m-b-10 m-r-20">楼+</div>
              <div class="b-r-text m-t-10 m-b-10 m-r-20">会员</div>
              <div class="j-flex al-cnter m-t-10 m-b-10">
                <div class="b-r-text ">社区</div>
                <i class="iconfont icon-down icon-dropdown"></i>
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
  props: {},
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
.frame {
  width: 100%;
  height: 100%;
  background-color: rgb(249, 249, 249);
  box-shadow: 1px -1px 14px #eee;
}
.frame-center {
  width: 1140px;
}
.top {
  margin: 15px 0 20px;
}
img {
  width: 150px;
}
.text12 {
  height: 50px;
}
.text1,
.text2 {
  &:hover {
    color: rgb(84, 193, 133);
    cursor: pointer;
  }
}
.text3 {
  width: 80px;
  height: 50px;
  color: rgb(84, 193, 133);
  &:hover {
    color: rgb(153, 153, 153);
    cursor: pointer;
  }
}
.text4 {
  width: 80px;
  height: 50px;
  background-color: rgb(84, 193, 133);
  color: #fff;
  &:hover {
    cursor: pointer;
  }
}
.line {
  width: 1px;
  height: 12px;
  background-color: rgb(153, 153, 153);
}
.b-left {
  width: 260px;
  height: 64px;
  background-color: rgb(8, 191, 145);
}
.b-rigth {
  width: 880px;
  height: 64px;
  background-color: #fff;
}
.icon-All {
  font-size: 18px !important ;
  color: #fff;
  height: 30px;
}
.icon-dropdown{
    font-size: 18px !important;
}
</style>