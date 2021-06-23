<template>
  <div class="list">
    <GoodsListItem v-for="item in goods" :key="item.page" :goodsItem="item"/>
  </div>
</template>

<script>
import GoodsListItem from "./GoodsItem"
export default {
  name:'Goods',
  components:{
    GoodsListItem
  },
  props:{
    goods:{
      type:Array,
      default() {
        return[]
      }
    }
  }
}
</script>

<style>
  .list {
   display: flex;
   flex-wrap: wrap;
   justify-content: space-around;
  }
</style>