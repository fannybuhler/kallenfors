<template>
  <div class="featured-skill">
    <img class="featured-skill__icon" :src="imageUrl" />
    <div class="featured-skill__text">
      <h3 class="featured-skill__heading">{{ heading }}</h3>
      <p class="featured-skill__body">{{ leading }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    heading: String,
    leading: String,
    image: String,
  },

  computed: {
    imageUrl () {
      if (this.$props.image.includes('https')) {
        return this.$props.image
      }

      return require(`@/assets/images/${this.$props.image}`)
    }
  }
}
</script>
