<template>
 <div>
   <div v-for="(item,index) in arr.slice(0,1) " :key="index">
    <img :src="item.picture_url" alt="">
   
   </div>
 </div>
</template>

<script>
 export default {
   name: '',
   props: {
     arr:{
       type:Array
     }
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

</style>