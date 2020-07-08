<template>
  <div>
    <div class="fonnts j-center">
      <div class="fonnts-center">
        <div>
          <div>
            <img src="../../assets/imgs/4a4ab3d.svg" alt />
          </div>
          <div class="text1 m-t-10 m-b-10">动手做实验，轻松学IT</div>
          <div class="j-flex">
            <div class="weixin j-center al-cnter m-r-10">
              <img src="../../assets/imgs/8832e65.svg" alt class="img1" />
            </div>
            <div class="weixin j-center al-cnter">
              <img src="../../assets/imgs/8832e65.svg" alt class="img1" />
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
.fonnts {
  background-color: rgb(51, 51, 51);
  height: 450px;
  .fonnts-center {
    width: 1140px;
  }
}
.text1 {
  color: rgb(8, 191, 145);
  font-size: 26px;
}
.weixin {
  width: 40px;
  height: 40px;
  border-radius: 50px;
  background-color: rgba(255, 255, 255, 0.2);
}
.img1 {
  width: 20px;
  height: 20px;
}
</style>