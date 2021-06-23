<template>
  <div>
    <Swiper v-model="selected" autoplay>
      <SwiperItem name="box1">
        <a :href="this.banners[0].link">
          <img  class="content" :src="this.banners[0].image" alt="">
        </a>
      </SwiperItem>

      <SwiperItem name="box2">
        <a :href="this.banners[1].link">
          <img class="content" :src="this.banners[1].image" alt="">
        </a>
      </SwiperItem>

      <SwiperItem name="box3">
        <a :href="this.banners[2].link">
          <img class="content" :src="this.banners[2].image" alt="">
        </a>
      </SwiperItem>

      <SwiperItem name="box4">
        <a :href="this.banners[3].link">
          <img class="content" :src="this.banners[3].image" alt="">
        </a>
      </SwiperItem>
    </Swiper>
  </div>
</template>

<script>
import { Swiper, SwiperItem } from "@/components/common/swiper/index.js";

export default {
  name:'MySwiper',
  components:{
    Swiper,
    SwiperItem
  },
  props:{
    banners:{}
  },
  data(){
    return { 
      selected: "box1",
     };
  },
}
</script>

<style>
  .content {
  width: 100%;
  height: 150px;
  text-align: center;
  margin: auto;
}
</style>