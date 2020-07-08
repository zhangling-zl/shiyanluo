<template>
  <div>
  
  </div>
</template>

<script>
export default {
  name: "",
  props: {},
  components: {},
  data() {
    return {
      Sorts: {
        type: Object
      }
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
</style>