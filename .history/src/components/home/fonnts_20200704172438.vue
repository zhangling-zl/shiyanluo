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
          <div class="text11">公司</div>
          <div class="text22">关于我们</div>
          <div class="text22">联系我们</div>
          <div class="text22">加入我们</div>
        </div>
          <div class="tow">
          <div class="text11">合作</div>
          <div class="text22">成为作者</div>
          <div class="text22">教师合作</div>
          <div class="text22">友情链接</div>
          <div class="text22">开发者</div>
        </div>
          <div class="tow">
          <div class="text11">服务</div>
          <div class="text22">企业版</div>
          <div class="text22">实战训练营</div>
          <div class="text22">会员服务</div>
          <div class="text22">实验报告</div>
          <div class="text22">常见问题</div>
          <div class="text22">隐私条款</div>
        </div>
          <div class="tow">
          <div class="text11">学习路径</div>
          <div class="text22">Linuxux学习路径</div>
          <div class="text22">大数据学习路径</div>
          <div class="text22">Java学习路径</div>
          <div class="text22">PHP学习路径</div>
          <div class="text22">全部</div>
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
  .fonnts-center {
    width: 1140px;
    padding: 20px;
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
.text11{
    color: rgb(153,153,153);
    font-size: 18px;
    margin-bottom: 15px;
}
.text22{
    color: rgb(153,153,153);
    font-size: 14px;
    margin-bottom: 5px;
}
</style>