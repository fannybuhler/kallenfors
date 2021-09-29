<template>
  <div>
    <PersonHero
      :image="hero.image"
      :alt="hero.alt"
      :heading="hero.heading"
      :role="hero.role"
      :location="hero.location"
      :phone="hero.phone"
      :mail="hero.mail"
    />
    <FeaturedSkills 
      heading="Expertis"
      :skills="skills"
    />
    <PromoCards
      heading="Erfarenhet"
      :items="items"
    />
  </div>
</template>

<script>
import items from '@/data/experience-peter'
import skills from '@/data/featured-skills-peter'
import hero from '@/data/hero-peter'

export default {
  data () {
    return {
      items,
      skills,
      hero
    }
  }
}
</script>

<style>

</style>
