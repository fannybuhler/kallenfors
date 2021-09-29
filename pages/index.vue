<template>
  <div>
    <LandingPage />
    <AboutUs />
    <IntroLeft />
    <Intro
      modifier="image-left"
      :link="introPeter.link"
      :alt="introPeter.alt"
      :name="introPeter.name"
      :image="introPeter.image"
      :heading="introPeter.heading"
      :description="introPeter.description"
    />
    <Intro
      modifier="image-right"
    />
    <IntroLeft2 />
    <FeaturedSkills
      heading="Expertis"
      :skills="skills"
    />
    <IntroRight />
    <Carousel />
  </div>
</template>

<script>
import items from '@/data/experience-peter'
import skills from '@/data/featured-skills-peter'
import introPeter from '@/data/intro-peter'

export default {
  data () {
    return {
      items,
      skills,
      introPeter
    }
  }
}
</script>
