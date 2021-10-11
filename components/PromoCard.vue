<template>
  <div class="promo-card">
    <img class="promo-card__image" :src="imageUrl" />
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
  &__image {
    width: 100%;
    display: block;
  }

  &__info {
    margin-top: 1rem;
  }

  &__heading {
    @include h4();
  }

  &__leading {
    //
  }

  &__meta {
    margin: 1rem 0 0;
  }

  &__tag {
    font-size: 14px;
    color: #696969;
    // padding: 0.5rem 1rem;
    // background: rgba(#000, 0.1);
    // margin: 0.5rem 0.5rem 0 0;
    // border-radius: 0.5rem;
  }
}
</style>
