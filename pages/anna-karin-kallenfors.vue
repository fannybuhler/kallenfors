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
    <br>
    <PromoCards
      heading="Erfarenhet"
      :items="items"
    />
    <br>
    <FeaturedSkills 
      heading="Expertis"
      :skills="skills"
    />
  </div>
</template>

<script>
import items from '@/data/experience-ak'
import skills from '@/data/featured-skills-ak'
import hero from '@/data/hero-ak'

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
