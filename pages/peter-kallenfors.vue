<template>
  <div>
    Peter Källenfors
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
import items from '@/data/experience-peter'
import skills from '@/data/featured-skills-peter'

export default {
  data () {
    return {
      items,
      skills
    }
  }
}
</script>

<style>

</style>
