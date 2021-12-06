<template>
  <swiper class="carousel-card" ref="mySwiper" :options="swiperOptions">
    <swiper-slide v-for="slides, index in carousel" :key="index">
      <CarouselSlide 
        :image="slides.image"
        :alt="slides.alt"
        :heading="slides.heading"
        :leading="slides.leading"
        :link="slides.link"
        :name="slides.name"
        :dark="slides.dark"
      />
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
import 'swiper/css/swiper.css';

export default {
  name: 'carousel',

  props: {
    carousel: {
      type: Array,
      default: () => []
    }
  },

  data() {
    return {
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
        }
      },
    }
  },

  computed: {
    swiper() {
      return this.$refs.mySwiper.$swiper
    }
  },
}
</script>

<style lang="scss" scoped>

</style>
