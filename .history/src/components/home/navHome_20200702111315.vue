<template>
  <div>
    <div class="frame j-center">
      <div class="frame-center j-between">
        <div class="left f-18 j-center al-cnter">
          <img src="../../assets/imgs/9f43b00.svg" alt="logo" />
          <div>做实验，学编程</div>
        </div>
        <div class="rigth j-center">
          <div>企业版</div>
          <div></div>
          <div>学校版</div>
          <div>登录</div>
          <div class="text4">注册</div>
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
}
.frame-center {
  width: 1140px;
}
img {
  width: 150px;
}
.text4{
    width: 80px;
    height: 50px;
    background-color: rgb(84,193,133);
    color: #fff;
}
</style>