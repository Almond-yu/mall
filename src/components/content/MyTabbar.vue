<template>
  <Tabbar>
      <TabbarItem path="/home" activeColor="red">
      <img slot="item-icon" src="@/assets/img/tabbar/home.png" alt="">
      <img slot="item-icon-active" src="@/assets/img/tabbar/home-active.png" alt="">
      <div slot="item-text">首页</div>
      </TabbarItem>

      <TabbarItem path="/category" activeColor="red">
      <img slot="item-icon" src="@/assets/img/tabbar/class.png" alt="">
      <img slot="item-icon-active" src="@/assets/img/tabbar/class-active.png" alt="">
      <div slot="item-text">分类</div>
      </TabbarItem>

      <TabbarItem path="/cart" activeColor="red">
      <img slot="item-icon" src="@/assets/img/tabbar/shopping.png" alt="">
      <img slot="item-icon-active" src="@/assets/img/tabbar/shopping-active.png" alt="">
      <div slot="item-text">购物车</div>
      </TabbarItem>

      <TabbarItem path="/profile" activeColor="red">
      <img slot="item-icon" src="@/assets/img/tabbar/my.png" alt="">
       <img slot="item-icon-active" src="@/assets/img/tabbar/my-active.png" alt="">
      <div slot="item-text">我的</div>
      </TabbarItem>
   </Tabbar>
</template>

<script>
import Tabbar from '@/components/common/tabbar/Tabbar'
import TabbarItem from '@/components/common/tabbar/TabbarItem'
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