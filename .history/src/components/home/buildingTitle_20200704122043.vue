<template>
  <div>
    <div class="title j-center">
      <div class="title-center">
        <div class="big">
          <slot name="big"></slot>
        </div>
        <div>
          <slot name="small"></slot>
        </div>
        <div class="line m-l-10 m-r-10"></div>
        <div>
            <slot name="more"></slot> 
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
.title {
  background-color: rgb(249, 249, 249);
  height: 100px;
  .title-center {
    width: 1140px;
  }
}
.line {
  width: 2px;
  height: 20px;
  background-color: rgb(0, 0, 0);
}
.big{
    color: rgb(86, 86, 86);
    font-size: 24px;
}
</style>