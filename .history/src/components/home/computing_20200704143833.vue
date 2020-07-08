<template>
  <div>
    <div class="boxs j-center">
      <div class="boxs-center">
        <div v-if="this.keys.length!==0">
          <div>
            <img :src="this.Sorts.recommend_course.picture_url" alt class="img11" />
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
  height: 250px;
  box-shadow: 1px 1px 2px #ccc;
  &:hover {
    box-shadow: 1px 1px 20px #ccc;
  }
}
</style>