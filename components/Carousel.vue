<template>
  <swiper class="carousel-card" ref="mySwiper" :options="swiperOptions" :navigation="true">
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
    <div slot="pagination" class="swiper-pagination" ></div>
    <div slot="button-prev" class="swiper-button-prev"></div>
    <div slot="button-next" class="swiper-button-next"></div>
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
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
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
