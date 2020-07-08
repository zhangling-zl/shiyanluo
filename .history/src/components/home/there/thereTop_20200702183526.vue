<template>
 <div>
   <div class="cnter1 j-center">
     <div class="c1-center j-between al-cnter m-t-b-30">
       <div class="c1-c-text j-flex al-cnter">
         <div class="c1-c-text1 f-24">{{title1}}</div>
         <div class="line1 m-l-r-10"></div>
         <div class="c1-c-text2 f-14">{{title2}}</div>
       </div>
       <div class="c1-c-text3 f-14">更多&gt;&gt;</div>
     </div>
   </div>
 </div>
</template>

<script>
import axios from "axios";
 export default {
   name: '',
   props: {
     title1:{
       type:String
     },
     title2:{
       type:String
     },
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
.cnter1{
   background-color: rgb(249,249,249);
   .c1-center{
     width: 1140px;
   }
}
.line1{
  width: 2px;
  height: 20px;
  background-color: rgb(0,0,0);
}
.c1-c-text1{
  color: rgb(86,86,86);
}
.c1-c-text2{
  color: rgb(86,86,86);
}
.c1-c-text3{
  color: rgb(86,86,86);
}


</style>