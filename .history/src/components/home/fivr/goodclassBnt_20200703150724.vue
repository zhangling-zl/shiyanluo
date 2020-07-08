<template>
 <div>
   <div v-for="(item,index) in img1.slic(8)" :key="index"></div>
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