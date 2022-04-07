<template>
  <div class="interim">
    <SubpageHero
      :color="hero.color"
      :image="hero.image"
      :alt="hero.alt"
      :heading="hero.heading"
      :description="hero.description"
      :externalLink="hero.externalLink"
    />
  </div>
</template>

<script>
import hero from '@/data/hero-terapihundar'

export default {
  data () {
    return {
      hero
    }
  }
}
</script>