<template>
  <div class="promo-card">
    <img class="promo-card__icon" :src="imageUrl" />
    <div class="promo-card__text">
      <h3 class="promo-card__heading">{{ heading }}</h3>
      <p class="promo-card__body">{{ leading }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    heading: String,
    leading: String,
    image: String,
    tags: Array
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
