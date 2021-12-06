<template>
  <div class="promo-card">
    <div class="promo-card__size">
      <img class="promo-card__image" :src="imageUrl" />
    </div>
    <div class="promo-card__info">
      <h3 class="promo-card__heading">{{ heading }}</h3>
      <p class="promo-card__leading">{{ leading }}</p>
      <p class="promo-card__meta">
        <span v-for="tag, index in tags" :key="index" v-text="tag" class="promo-card__tag" />
      </p>
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

<style lang="scss" scoped>
.promo-card {
  &__size {
    width: 100%;
    height: 250px;
    background-color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  &__image {
    height: auto;
    width: auto;
    max-width: 70%;
    max-height: 80%;
  }

  &__info {
    margin-top: 1rem;
  }

  &__heading {
    @include h4();
  }

  &__tag {
    font-size: 14px;
    color: #696969;
  }
}
</style>
