<template>
  <div class="tab-control">
    <div v-for="(item,index) in title" :key="item" 
    class="tab-control-item"
    :class="{active: index === currentIndex}"
    @click="itemClick(index)">
      <span>{{item}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name:'tabControl',
  data(){
    return {
      currentIndex:0
    }
  },
  props:{
    title:{
      type:Array,
      default (){
        return []
      }
    },
  },
  methods:{
    itemClick(index){
      this.currentIndex=index;
    }
  }
}
</script>

<style>
  .tab-control{
    display:flex;
    text-align: center; 
    font-size: 15px;
    height: 40px;
    line-height: 40px;
    background-color: #fff;
    z-index: 9;
    /* 距离父元素44px使用fixed属性 */
    position:sticky;
    top:44px;
  }
  .tab-control-item {
    flex:1;
  }
  .active{
    color: rgb(254,195,205)
    
  }
  .active span {
    border-bottom: 3px solid rgb(254,195,205)
  }
</style>