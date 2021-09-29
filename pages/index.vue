<template>
  <div>
    <LandingPage />
    <AboutUs />
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
      :link="introAk.link"
      :alt="introAk.alt"
      :name="introAk.name"
      :image="introAk.image"
      :heading="introAk.heading"
      :description="introAk.description"
    />
  </div>
</template>

<script>
import introPeter from '@/data/intro-peter'
import introAk from '@/data/intro-ak'

export default {
  data () {
    return {
      introPeter,
      introAk
    }
  }
}
</script>
