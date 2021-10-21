<template>
  <div class="marknadsforing">
    <SubpageHero 
      :color="hero.color"
      :image="hero.image"
      :alt="hero.alt"
      :heading="hero.heading"
      :description="hero.description"
    />
  </div>
</template>

<script>
import hero from '@/data/marknadsforing-hero'

export default {
  data () {
    return {
      hero
    }
  }
}
</script>

<style lang="scss" scoped>
.marknadsforing {
  @include pageWrap();
}
</style>
