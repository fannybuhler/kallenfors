<template>
  <div class="featured-skills">
    <h2 v-if="heading" class="featured-skills__heading" v-text="heading" />
    <div class="featured-skills__list">
      <div class="featured-skills__item" v-for="skill, index in skills" :key="index">
        <FeaturedSkill
          :heading="skill.heading"
          :leading="skill.leading"
          :image="skill.image"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    heading: {
      type: String,
      default: ''
    },
    skills: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style lang="scss" scoped>
.featured-skills {
  @include boxer(red, 0, 2);
  @include mainContent();

  &__heading {
    @include h2();
    margin-bottom: 1rem;
  }

  &__list {
    display: grid;
    grid-gap: 3rem;

    @media only screen and (min-width: $tablet) {
      display: grid;
      grid-gap: 3rem 1.5rem;
      grid-template-columns: repeat(3, 1fr);
    }
  }

  &__item {
    //
  }
}
</style>
