<template>
  <div>
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
import hero from '@/data/interimsuppdrag-hero'
import items from '@/data/experience-interim'

export default {
  data () {
    return {
      hero,
      items
    }
  }
}
</script>
