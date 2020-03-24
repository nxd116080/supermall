<!-- 轮播图集中在这里，然后放进Home组件 -->
<template>
  <swiper>
    <swiper-item v-for="item in banners" :key="item.id">
      <a :href="item.link">
        <img :src="item.image" alt="">
      </a>
    </swiper-item>
  </swiper>
</template>

<script>
  import Swiper from 'components/common/swiper/Swiper'
  import SwiperItem from 'components/common/swiper/SwiperItem'

export default {
  name: 'HomeSwiper',
  props: {
    banners: {
      type: Array,
      default() {
        return []
      }
    }
  },
  components: {
    Swiper,
    SwiperItem
  },
}
</script>
<style scoped>
/* @import url(); 引入css类 */

</style>