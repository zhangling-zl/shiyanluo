<template>
 <div>
   <navHome></navHome>
   <bannerHome></bannerHome>
 </div>
</template>

<script>
import navHome from '../components/home/navHome'
import bannerHome from '../components/home/bannerHome'
import axios from 'axios'
 export default {
   name: '',
   props: {
   },
   components: {
     navHome,
     bannerHome

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