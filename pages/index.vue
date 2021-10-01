<template>
  <div>
    <LandingPage />
    <AboutUs />
    <Intro
      modifier="image-left"
      :link="introPeter.link"
      :alt="introPeter.alt"
      :firstName="introPeter.firstName"
      :lastName="introPeter.lastName"
      :image="introPeter.image"
      :heading="introPeter.heading"
      :description="introPeter.description"
    />
    <Intro
      modifier="image-right"
      :link="introAk.link"
      :alt="introAk.alt"
      :firstName="introAk.firstName"
      :lastName="introAk.lastName"
      :image="introAk.image"
      :heading="introAk.heading"
      :description="introAk.description"
    />
    <Carousel 
      :carousel="carousel"
    />
  </div>
</template>

<script>
import introPeter from '@/data/intro-peter'
import introAk from '@/data/intro-ak'
import carousel from '@/data/carousel'

export default {
  data () {
    return {
      introPeter,
      introAk,
      carousel
    }
  }
}
</script>
