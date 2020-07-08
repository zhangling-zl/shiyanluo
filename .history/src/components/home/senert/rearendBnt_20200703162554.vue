<template>
 <div>
   <div v-for="(item,index) in img1" :key="index">
    <div><img :src="item.courses.picture_url" alt=""></div>
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