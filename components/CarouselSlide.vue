<template>
  <div class="carousel">
    <div class="carousel__media">
      <!-- <img class="carousel__image" :src="imageUrl" :alt="alt"> -->
    </div>
    <div class="carousel__content">
      <h3 class="carousel__heading">Heading: {{ heading }}</h3>
      <p class="carousel__leading">Leading: {{ leading }}</p>
      <button class="carousel__button">
        <NuxtLink to="link">Läs mer</NuxtLink>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    image: String, 
    alt: String,
    heading: String,
    leading: String,
    link: String,
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

<style lang="scss" scoped>
.carousel {
  @include box(red);

  &__button {
    background: $pop;
    border: none;
    width: fit-content;
    padding: 10px 15px;
    text-transform: uppercase;
    font-weight: 400;
    letter-spacing: 4px;
    color: #000;
  }
}
</style>