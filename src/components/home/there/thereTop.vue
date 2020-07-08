<template>
  <div>
    <div class="thereTop j-center">
      <div class="t-center">
        <div class="t-c-top j-between al-cnter m-t-30 m-b-30">
          <div class="t-c-t-left j-flex al-cnter">
            <div class="c1-c-text1 f-24">{{title1}}</div>
            
            <div class="c1-c-text2 f-14 m-l-10">{{title2}}</div>
          </div>
          <div class="c1-c-text3 f-14">更多&gt;&gt;</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {
    title1: {
      type: String
    },
    title2: {
      type: String
    }
  },
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
.thereTop {
  background-color: rgb(249, 249, 249);
  .t-center {
    width: 75%;
  }
}
.line {
  width: 2px;
  height: 20px;
  background-color: rgb(0, 0, 0);
}
.c1-c-text1 {
  color: rgb(86, 86, 86);
}
.c1-c-text2 {
  color: rgb(86, 86, 86);
}
.c1-c-text3 {
  color: rgb(86, 86, 86);
}
</style>