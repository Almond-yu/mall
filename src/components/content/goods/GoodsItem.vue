<template>
  <div class="item">
    <img :src="goodsItem.link" alt="" class="image" />
  <div class="info">
    <p>{{ goodsItem.details }}</p>
    <span class="price">{{ goodsItem.price}}￥</span>
    <span class="score">评分:{{ goodsItem.score }}</span>
  </div>
</div>
</template>

<script>
export default {
  name: "GoodsListItem",
  props: {
    goodsItem: {
      type: Object,
      default() {
        return {};
      },
    },
  },
};
</script>

<style>
.item {
  width: 48%;
}
.item img {
  width: 100%;
  border-radius: 5px;
}
.info {
  font-size: 14px;
  overflow: hidden;
  text-align: center;
}
.info p {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  margin-bottom: 3px;
}
</style>