<template>
  <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide v-for="slides, index in carousel" :key="index">
      {{ index }}
      <CarouselSlide 
        :image="carousel.image"
        :alt="carousel.alt"
        :heading="carousel.heading"
        :leading="carousel.leading"
        :link="carousel.link"
      />
    </swiper-slide>
    <!-- <swiper-slide>Slide 2</swiper-slide>
    <swiper-slide>Slide 3</swiper-slide>
    <swiper-slide>Slide 4</swiper-slide>
    <swiper-slide>Slide 5</swiper-slide> -->
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

  mounted() {
    console.log('Current Swiper instance object', this.swiper)
    // this.swiper.slideTo(3, 1000, false)
  }
}
</script>

<style lang="scss" scoped>
.carousel-card {
  @include box(red);
  padding: 12rem 0;
}
</style>
