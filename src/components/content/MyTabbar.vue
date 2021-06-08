<template>
  <Tabbar>
      <TabbarItem path="/home" activeColor="red">
      <img slot="item-icon" src="@/assets/img/home.png" alt="">
      <img slot="item-icon-active" src="@/assets/img/home-active.png" alt="">
      <div slot="item-text">首页</div>
      </TabbarItem>

      <TabbarItem path="/category" activeColor="red">
      <img slot="item-icon" src="@/assets/img/class.png" alt="">
      <img slot="item-icon-active" src="@/assets/img/class-active.png" alt="">
      <div slot="item-text">分类</div>
      </TabbarItem>

      <TabbarItem path="/cart" activeColor="red">
      <img slot="item-icon" src="@/assets/img/shopping.png" alt="">
      <img slot="item-icon-active" src="@/assets/img/shopping-active.png" alt="">
      <div slot="item-text">购物车</div>
      </TabbarItem>

      <TabbarItem path="/profile" activeColor="red">
      <img slot="item-icon" src="@/assets/img/my.png" alt="">
       <img slot="item-icon-active" src="@/assets/img/my-active.png" alt="">
      <div slot="item-text">我的</div>
      </TabbarItem>
   </Tabbar>
</template>

<script>
import Tabbar from '@/components/common/Tabbar'
import TabbarItem from '@/components/common/TabbarItem'
export default {
  name:'Mytabbar',
  components:{
    Tabbar,
    TabbarItem
  }
}
</script>

<style>

</style>