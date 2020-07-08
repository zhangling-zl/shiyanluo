<template>
  <div>
    <div class="title j-center">
      <div class="title-center">
        <div class="big">
          <slot name="big"></slot>
        </div>
        <div></div>
        
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
  .title-center {
    width: 1140px;
  }
}
</style>