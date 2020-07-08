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
            <div class="j-flex m-l-20 al-cnter">
              <i class="iconfont icon-gengduo1 icon-All m-r-10"></i>
              <div class="b-text fff">全部课程</div>
            </div>
          </div>
          <div class="b-rigth j-between al-cnter">
            <div class="b-rigth-text j-flex ">
              <div class="b-r-text ">路径</div>
              <div class="b-r-text ">训练营</div>
              <div class="b-r-text ">楼+</div>
              <div class="b-r-text ">会员</div>
              <div class="j-flex al-cnter" @mouseenter="enter" @mouseleave="leave">
                <div class="b-r-text">
                  社区
                  <i class="iconfont icon-down icon-dropdown"></i>
                  <div class="fkfk" v-if="flge===true">
                    <div class="n-c-rigth-left-text-1">讨论</div>
                    <div class="n-c-rigth-left-text-1">教程库</div>
                    <div class="n-c-rigth-left-text-1">直播</div>
                    <div class="n-c-rigth-left-text-1 b-b-l-r b-b-r-r">比赛</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="b-rigth-search m-r-15">
              <input type="text" placeholder="搜索 课程/问答" class="input" />
              <i class="iconfont icon-sousuo icon-search"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="navBnt j-center">
    <div class="navBnt-center"></div></div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {},
  components: {},
  data() {
    return {
      flge: false
    };
  },
  methods: {
    //鼠标移入事件
    enter() {
      this.flge = true;
    },
    //鼠标移出事件
    leave() {
      this.flge = false;
    }
  },
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
.top {
  margin: 15px 0 20px;
}
img {
  width: 130px;
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
  position: relative;
}
.icon-All {
  font-size: 18px !important ;
  color: #fff;
}

.input {
  position: relative;
  width: 180px;
  outline: none;
  border: none;
  border: 1px solid rgb(206, 212, 218);
  border-radius: 4px;
  padding: 8px 8px;
  color: rgb(153, 153, 153);
  &:hover {
    border: 1px solid rgb(8, 191, 145);
    box-shadow: 1px 1px 1px #eee;
  }
}
.icon-search {
  position: absolute;
  right:20px;
  top: 24px;
}
.b-r-text{
   display: flex;
  justify-content: center;
  align-items: center;
  height: 64px;
  margin: 0px 2px;
  padding: 0px 10px;
  font-size: 18px;
  color: rgb(58, 58, 58);
  &:hover {
    color: rgb(8, 191, 145);
    cursor: pointer;
  }
  .icon-dropdown {
    font-size: 18px !important;
  }
}
.fkfk {
  border-radius: 0 0 10px 10px;
  background-color: #fff;
  width: 150px;
  position: absolute;
  top: 64px;
  left: 276px;
  z-index: 99;
  
}
.n-c-rigth-left-text-1 {
  height: 45px;
  display: flex;
  align-items: center;
  padding-left: 15px;
  color: #333;
  &:hover {
    background: rgb(247, 247, 247);
    color: rgb(8, 191, 145);
  }
}
.navBnt{
  width: 100%;
  height: 70px;
   background-color: #fff;
  box-shadow: -1px 20px 10px #ccc;
  .navBnt-center{
    width: 1140px;
    background-color: #ccc;
  }
}
</style>