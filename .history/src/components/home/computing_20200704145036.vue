<template>
  <div>
    <div class="boxs j-center">
      <div class="boxs-center j-between">
        <div v-if="this.keys.length!==0">
          <div>
            <img :src="this.Sorts.recommend_course.picture_url" alt class="img11" />
          </div>
        </div>
        <div class="from-box j-between ">
          <div v-for="(item,index) in arr" :key="index">
            <div class="from m-b-10">
              <img :src="item.picture_url" alt class="img22" />
              <div class="title j-center al-cnter">
                <div>
                  <div class="title1">{{item.name}}</div>
                  <div class="title2 f-12">{{item.description}}</div>
                </div>
              </div>
              <div class="text j-between al-cnter">
                <div class="j-flex al-cnter m-l-5">
                  <i class="iconfont icon-jiaoyin jiaoyin m-r-10"></i>
                  <div class="text1 f-12">{{item.students_count}}次</div>
                </div>
                <div class="text2 j-center al-cnter f-12 m-r-10" v-if="item.price>0">训练营</div>
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
    Sorts: {
      type: Object
    }
  },
  components: {},
  data() {
    return {
      arr: [],
      keys: ""
    };
  },
  methods: {},
  mounted() {
    if (this.Sorts.courses.length > 6) {
      this.arr = this.Sorts.courses.slice(0, 6);
    } else {
      this.arr = this.Sorts.courses;
    }
    this.keys = Object.keys(this.Sorts.recommend_course);
  },
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
.img11 {
  width: 260px;
  height: 520px;
  box-shadow: 1px 1px 2px #ccc;
  &:hover {
    box-shadow: 1px 1px 20px #ccc;
  }
}
.from {
  width: 260px;
  height: 250px;
  background-color: #fff;
  position: relative;
  box-shadow: 1px 1px 2px #ccc;
  &:hover {
    box-shadow: 1px 1px 20px #ccc;
    .title2 {
      transition: all 0.5s;
      height: 66px;
    }
  }
}
.img22 {
  width: 260px;
  height: 150px;
}

.title {
  width: 260px;
  position: absolute;
  bottom: 50px;
  background-color: #fff;
}
.title1 {
  height: 50px;
  width: 240px;
  display: flex;
  align-items: center;
  color: #333;
}
.title2 {
  width: 240px;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
  height: 0px;
  color: rgb(102, 102, 102);
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
.text3 {
  width: 50px;
  height: 20px;
  background-color: rgb(255, 197, 0);
  border-radius: 15px;
  color: #fff;
}
.text {
  width: 260px;
  height: 50px;
  position: absolute;
  bottom: 0;
}
.from-box{
  width: 850px;
  height: 520px;
  flex-wrap: wrap;
}
</style>