<template>
  <div class="juridik">
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
import hero from '@/data/juridik-hero'

export default {
  data () {
    return {
      hero
    }
  }
}
</script>

<style lang="scss" scoped>
.juridik {
  @include pageWrap();
}
</style>
