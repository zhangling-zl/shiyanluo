<template>
  <div>
    <div class="fonnts j-center">
      <div class="fonnts-center j-between">
        <div class="one">
          <div>
            <img src="../../assets/imgs/4a4ab3d.svg" alt />
          </div>
          <div class="text1 m-t-20 m-b-20">动手做实验，轻松学IT</div>
          <div class="j-flex">
            <div class="weixin j-center al-cnter m-r-10">
              <img src="../../assets/imgs/8832e65.svg" alt class="img1" />
            </div>
            <div class="weixin j-center al-cnter">
              <img src="../../assets/imgs/8832e65.svg" alt class="img1" />
            </div>
          </div>
        </div>
        <div class="tow">
          <div>公司</div>
          <div>关于我们</div>
          <div>联系我们</div>
          <div>加入我们</div>
        </div>
          <div class="tow">
          <div>合作</div>
          <div>成为作者</div>
          <div>教师合作</div>
          <div>友情链接</div>
          <div>开发者</div>
        </div>
          <div class="tow">
          <div>服务</div>
          <div>企业版</div>
          <div>实战训练营</div>
          <div>会员服务</div>
          <div>实验报告</div>
          <div>常见问题</div>
          <div>隐私条款</div>
        </div>
          <div class="tow">
          <div>学习路径</div>
          <div>Linuxux学习路径</div>
          <div>大数据学习路径</div>
          <div>Java学习路径</div>
          <div>PHP学习路径</div>
          <div>全部</div>
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
.one {
  width: 350px;
}
.tow {
  width: 160px;
}
</style>