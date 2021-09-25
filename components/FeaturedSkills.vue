<template>
  <div class="featured-skills">
    <h2 v-if="heading" class="featured-skills" v-text="heading" />
    <div v-for="skill, index in skills" :key="index">
      <FeaturedSkill
        :heading="skill.heading"
        :leading="skill.leading"
        :image="skill.image"
      />
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
  @include boxer(red);
}
</style>
