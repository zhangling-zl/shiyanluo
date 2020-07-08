<template>
  <div>
    <div class="boxs j-center">
      <div class="boxs-center j-between">
        <div v-if="this.keys.length!==0">
          <div>
            <img :src="this.Sorts.recommend_course.picture_url" alt />
          </div>
        </div>
        <div v-for="(item,index) in arr" :key="index">
          <div class="from m-b-30">
            <img :src="item.picture_url" alt class="img22" />
            <div>
              <div class="title1">{{item.name}}</div>
              <div class="title2 f-12">{{item.description}}</div>
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
      this.arr = this.Sorts.courses.slice(0, 4);
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
.from {
  width: 260px;
  height: 250px;
  background-color: #fff;
  position: relative;
  box-shadow: 1px 1px 2px #ccc;
}
.img22 {
  width: 260px;
  height: 150px;
}

  .img11 {
    width: 550px;
    height: 250px;

    box-shadow: 1px 1px 2px #ccc;
    &:hover {
      box-shadow: 1px 1px 20px #ccc;
    }
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
</style>