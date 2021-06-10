<template>
  <div id="home">
    <!-- 导航栏 -->
    <NavBar class="home-navbar">
      <div slot="center">购物街</div>
    </NavBar>
    <!-- 轮播图 -->
    <MySwiper/>

  </div>
</template>

<script>
import NavBar from "@/components/common/navbar/NavBar";
import { getHomeMultidata } from "@/network/home";
import MySwiper from "@/components/content/MySwiper";


export default {
  name: "Home",
  components: {
    NavBar,
    MySwiper
  },
  data() {
    return {
      //首页请求数据
      banners: [],
      recommends: [],
    };
  },
  mounted() {
    
  },
  created() {
    // 获取主页数据
    getHomeMultidata().then((res) => {
      this.banners = res.data.banner.list;
      this.recommends = res.data.recommend.list;
    });
  },
};
</script>

<style>
.home-navbar {
  background-color: pink;
  color: seashell;
}

</style>