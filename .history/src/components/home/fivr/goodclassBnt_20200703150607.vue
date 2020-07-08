<template>
 <div>
  <div v-for="(item,index) in courses" :key="index">
   <img :src="item." alt="">
  </div>
 </div>
</template>

<script>
 export default {
   name: '',
   props: {
     img1:{
       type:Array
     }
   },
   components: {

   },
   data () {
     return {
       courses:[]

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

</style>