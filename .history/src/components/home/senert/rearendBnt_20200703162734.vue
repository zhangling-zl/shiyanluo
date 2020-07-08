<template>
 <div>
   <div v-for="(item,index) in img1" :key="index">
    <div><img :src="item.picture_url" alt=""></div>
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
     this.courses=img1.courses

   },
   watch: {

   },
   computed: {

   }
 }
</script>

<style scoped lang='scss'>

</style>