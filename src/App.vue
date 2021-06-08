<template>
  <div id="app">
    <router-view></router-view>
    <MyTabbar/>
   
   
  </div>
</template>
  
<script>
import MyTabbar from "@/components/content/MyTabbar"
  export default{
    name:'app',
    components:{
      MyTabbar
    }
  }
</script>
  
<style>
@import "./assets/css/base.css";

</style>


