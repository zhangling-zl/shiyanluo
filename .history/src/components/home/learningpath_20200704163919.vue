<template>
  <div>
    <div class="boxs j-center">
      <div class="boxs-center">
        <div class="top j-between">
          <div v-for="(item) in paths" :key="item">
            <div class="from">
              <img :src="item.image" alt />
              <div class="text j-center al-cnter al-flex">
                <div class="f-18 text1 m-b-10">{{item.name}}</div>
                <div class="f-14 text2">{{item.courses_count}}门课程</div>
              </div>
            </div>
          </div>
        </div>
        <div class="bottom">
          <div v-for="(item) in pathsAll" :key="item">
            <div class="from">
              <img :src="item.image" alt />
              "text j-center al-cnter al-flex">
                <div class="f-18 text1 m-b-10">{{item.name}}</div>
                <div class="f-14 text2">{{item.courses_count}}门课程</div>
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
    paths: {
      type: Array
    }
  },
  components: {},
  data() {
    return {
        pathsAll:[
            {
                name:'丰富全面的计算机实验课程'
            },
            {
                name:'在线编程环境，1秒启动'
            },
            {
                name:'每天一个项目课，丰富你的项目经验'
            },{
                name:'有效学习时间，真实记录你的代码生涯'
            }
        ]
    };
  },
  methods: {},
  mounted() {},
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.boxs {
  background-color: rgb(249, 249, 249);
  .boxs-center {
    width: 1140px;
    flex-wrap: wrap;
  }
}
img {
  width: 260px;
  height: 130px;
}
.text {
  height: 120px;
}
.from {
  width: 260px;
  height: 250px;
  background-color: #fff;
  margin-bottom: 40px;
  box-shadow: 1px 1px 2px #ccc;
  &:hover {
    box-shadow: 1px 1px 30px #ccc;
    transform: translateY(-10px);
    transition: all 0.5s;
  }
}
.text2 {
  color: rgb(164, 164, 164);
}
.text {
  color: rgb(102, 102, 102);
}
</style>