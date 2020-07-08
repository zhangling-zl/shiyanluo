<template>
  <div>
    
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
</style>