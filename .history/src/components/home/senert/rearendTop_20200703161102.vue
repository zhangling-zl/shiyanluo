<template>
 <div>
    <div class="featuredTop j-center">
      <div class="featuredTop-center m-t-40 m-b-30">
        <div class="j-between al-cnter">
         
            <div class="c1-c-text1 f-24">
              <slot name="text7"></slot>
            </div>
          
          <div class="c1-c-text3 f-14">更多&gt;&gt;</div>
        </div>
      </div>
    </div>
 </div>
</template>

<script>
 export default {
   name: '',
   props: {
   },
   components: {

   },
   data () {
     return {

     }
   },
   methods: {

   },
   mounted() {

   },
   watch: {

   },
   computed: {

   }
 }
</script>

<style scoped lang='scss'>
.featuredTop {
  background-color: rgb(249, 249, 249);
  .featuredTop-center {
    width: 1140px;
  }
}
.line2 {
  width: 2px;
  height: 20px;
  background-color: rgb(0, 0, 0);
}
.c1-c-text1,
.c1-c-text3 {
  color: rgb(86, 86, 86);
}

</style>