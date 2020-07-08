<template>
 <div>
   <div v-for="(item,index) in img1.slic(0,1)" :key="index">
   <div v-for="(item1,index1) in item.courses.slice(8,13)" :key="index></div>
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