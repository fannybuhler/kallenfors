<template>
  <div class="ak">
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
      modifier="large-grid"
    />
    <PromoCards
      heading="Erfarenhet"
      :items="items"
    />
  </div>
</template>

<script>
import items from '@/data/experience-ak'
import skills from '@/data/featured-skills-ak'
import hero from '@/data/hero-ak'
import terapihundar from '@/data/terapihundar'

export default {
  data () {
    return {
      items,
      skills,
      hero,
      terapihundar
    }
  }
}
</script>

<style lang="scss" scoped>
.second-intro {
  @include mainContent();
  @include pageWrap();
  display: flex;
  flex-direction: column;
  align-items: flex-end;

  &__heading {
    @include h2();
  }

  &__span {
    background: black;
    height: 1px;
    width: 70%;
    margin-top: 1rem;
    position: relative;
    left: 5%;

    @media only screen and (min-width: $tablet) {
      width: 50%;
    }
  }
}

</style>
