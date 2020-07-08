<template>
  <div>
    <div class="boxs j-center">
      <div class="boxs-center">
        <div v-for="(item,index) in strengthen" :key="index">
          <div class="from-box j-flex">
            <img :src="item.picture_url" class="img" />
            <div class="from">
              <div class="text1 m-b-20">{{item.name}}</div>
              <div class="text2 f-14">{{item.description}}</div>

              <div>{{item.tags[0]+item.tags[1]}}</div>
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
    strengthen: {
      type: Array
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
.boxs {
  background-color: rgb(249, 249, 249);
  .boxs-center {
    width: 1140px;
    flex-wrap: wrap;
  }
}
.img {
  width: 455px;
  height: 250px;
}
.from {
  height: 250px;
  width: 685px;
  background-color: #fff;
}
.from-box {
  box-shadow: 1px 1px 2px #ccc;
  margin-bottom: 30px;
  &:hover {
    cursor: pointer;
    box-shadow: 1px 1px 20px #ccc;
  }
}
.text1 {
  color: rgb(98, 98, 98);
}
.text2 {
  color: rgb(98, 98, 98);
  line-height: 24px;
}
</style>