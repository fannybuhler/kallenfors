<template>
  <div class="index">
      <!-- <LandingPageNew /> -->
      <LandingPage />
    <div class="index-wrapper">
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
      <div class="carousel">
        <p class="carousel__leading">Gedigen erfarenhet</p>
        <h3 class="carousel__heading">Tidigare uppdrag</h3>
        <div class="carousel__color-block"></div>
      </div>
    </div>
    <client-only>
      <Carousel :carousel="carousel" />
    </client-only>
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

<style lang="scss" scoped>
.index-wrapper {
  @include pageWrap();
}

.carousel {
  @include mainContent();
  position: relative;
  margin-top: 3rem;

  &__heading {
    font-family: 'Playfair regular';
    font-size: 32px;
    line-height: 120%;
    font-weight: 400;
    position: relative;
    z-index: 2;
    text-transform: uppercase;
    padding-bottom: 1rem;

    @media only screen and (min-width: $tablet) {
      font-size: 48px;
    }
  }

  &__leading {
    text-transform: uppercase;
  }

  &__color-block {
    height: 40%;
    width: 90%;
    position: absolute;
    bottom: 0;
    left: 0;
    background: $pop;

    @media only screen and (min-width: $desktop) {
      width: 50%;
    }
  }
}
</style>
