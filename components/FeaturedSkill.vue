<template>
  <div class="featured-skill">
    <div class="featured-skill__icon">
      <img class="featured-skill__image" :src="imageUrl" alt="icon"/>
    </div>
    <div class="featured-skill__text">
      <h3 class="featured-skill__heading">{{ heading }}</h3>
      <div class="featured-skill__span" />
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

<style lang="scss" scoped>
.featured-skill {
  display: flex;
  width: fit-content;
  align-items: center;
  justify-content: center;

  &__icon {
    display: block;
    border: 1px solid black;
    border-radius: 50%;
    margin-right: 1rem;
    padding: 1.5rem;
  }

  &__image {
    display: block;
    max-width: 64px;
  }

  &__text {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  &__heading {
    @include h3();
  }

  &__span {
    background: $black;
    color: $black;
    height: 1px;
    width: 30px;
    margin: 5px 0;
  }

  &__body {
    font-size: 12px;
    word-break: 5;
    line-height: 140%;
  }
}
</style>
