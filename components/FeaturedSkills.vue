<template>
  <div class="featured-skills">
    <h2 v-if="heading" class="featured-skills__heading" v-text="heading" />
    <div class="featured-skills__list" :class="modifier ? `featured-skills__list--${modifier}` : '' ">
      <div class="featured-skills__item" v-for="skill, index in skills" :key="index">
        <FeaturedSkill
          :heading="skill.heading"
          :leading="skill.leading"
          :image="skill.image"
          :modifier="modifier"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    modifier: {
      type: String,
      default: ''
    },
    heading: {
      type: String,
      default: ''
    },
    skills: {
      type: Array,
      default: () => []
    },
  }
}
</script>

<style lang="scss" scoped>
.featured-skills {
  @include pageWrap();
  @include mainContent();
  @include blockPadding();

  &__heading {
    @include h2();
    margin-bottom: 1.5rem;
    position: relative;
  }

  &__list {
    display: grid;
    grid-gap: 3rem;

    @media only screen and (min-width: $tablet) {
      display: grid;
      grid-gap: 3rem 1.5rem;
      grid-template-columns: repeat(2, 1fr);

      &--large-grid {
        grid-template-columns: 1fr;
      }
    }

    @media only screen and (min-width: $desktop) {
      grid-template-columns: repeat(3, 1fr);

      &--large-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }
  }
}
</style>
