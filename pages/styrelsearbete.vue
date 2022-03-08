<template>
  <div class="styrelsearbete">
    <SubpageHero 
      :color="hero.color"
      :image="hero.image"
      :alt="hero.alt"
      :heading="hero.heading"
      :description="hero.description"
    />
    <PromoCards
      heading="Erfarenhet"
      :items="items"
    />
  </div>
</template>

<script>
import hero from '@/data/hero-styrelsearbete'
import items from '@/data/experience-styrelsearbete'

export default {
  data () {
    return {
      hero,
      items
    }
  }
}
</script>