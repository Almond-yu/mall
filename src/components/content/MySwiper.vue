<template>
  <div>
    <Swiper v-model="selected" autoplay>
      <SwiperItem name="box1">
        <img  class="content" src="@/assets/img/swiper/1.jpg" alt="">
      </SwiperItem>

      <SwiperItem name="box2">
        <img class="content" src="@/assets/img/swiper/2.jpg" alt="">
      </SwiperItem>

      <SwiperItem name="box3">
        <img class="content" src="@/assets/img/swiper/3.jpg" alt="">
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
  data(){
    return { selected: "box1" };
  }
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