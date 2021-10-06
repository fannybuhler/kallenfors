<template>
  <div>
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
import hero from '@/data/styrelsearbete-hero'

export default {
  data () {
    return {
      hero
    }
  }
}
</script>
