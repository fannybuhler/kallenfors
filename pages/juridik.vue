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
import hero from '@/data/hero-juridik'

export default {
  data () {
    return {
      hero
    }
  }
}
</script>

