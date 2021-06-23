<template>
  <div id="home">
    <!-- 导航栏 -->
    <NavBar class="home-navbar">
      <div slot="center">购物街</div>
    </NavBar>
    <!-- 轮播图 -->
      <MySwiper :banners="banners" v-if="banners.length!=0" class="swiper"></MySwiper>
      <Recommend :recommends="recommends"/>
      <TabControl :title="['流行','新款', '精选']"/>
      <Goods :goods="goods.pop.list"/>
      <ul>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
        <li>1</li>
      </ul>
  </div>

</template>

<script>
import NavBar from "@/components/common/navbar/NavBar";
import MySwiper from "@/views/home/homeChild/MySwiper";
import Recommend from "@/views/home/homeChild/Recommend"
import TabControl from "@/components/common/tabcontrol/TabControl"
import Goods from "@/components/content/goods/Goods"
import { getHomeMultidata, getHomeGoods } from "@/network/home";


export default {
  name: "Home",
  components: {
    NavBar,
    MySwiper,
    Recommend,
    TabControl,
    Goods
   
  },
  data() {
    return {
      //首页请求数据
      banners: [],
      recommends: [],
      goods:{
        "pop" : {page: 0,list: [
          {link:"https://img30.360buyimg.com/sku/jfs/t22816/203/505598751/332779/d34053f6/5b336fa2Nabc5d885.jpg",details:"手表",price:50,score:4.1},
          {link:"https://img30.360buyimg.com/sku/jfs/t22816/203/505598751/332779/d34053f6/5b336fa2Nabc5d885.jpg",details:"随着网络购物的兴起，成千上万的人开始在网络创业，而这部分人本身也就成为一个特定的消费群体。他们对于优质宝贝描述的需求也成就了宝贝描述的市场。网络上数量众多的装修店铺，宝贝模版销售等业务开展得如火如荼。",price:20,score:4.2},
          {link:"https://img30.360buyimg.com/sku/jfs/t22816/203/505598751/332779/d34053f6/5b336fa2Nabc5d885.jpg",details:"手表2",price:60,score:5.0}
        ]},
        "new" : {page: 0,list: []},
        "sell" : {page: 0,list: []}
      }
    };
  },
  methods:{
      getHomeMultidata(){
        getHomeMultidata().then((res) => {
        this.banners = res.data.banner.list;
        this.recommends = res.data.recommend.list;
      });
      },
      //接口无了
      // getHomeGoods(type){
      //   const page = this.goods[type].page+1;
      //   getHomeGoods(type,page).then((res)=>{
          
      //   })
      // },
    },
  mounted() {
    
  },
  created() {
    // 获取主页数据
    this.getHomeMultidata();
    // 获取商品数据(接口无了)
    // this.getHomeGoods('pop');
    // this.getHomeGoods('new');
    // this.getHomeGoods('sell');
  },
};
</script>

<style>
.home-navbar {
  background-color: pink;
  color: seashell;
  width: 100%;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
}
.swiper {
  padding-top: 20px;
}

</style>