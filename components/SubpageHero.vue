<template>
  <div class="subpage-hero">
    <div class="subpage-hero__color-block-wrapper">
      <div class="subpage-hero__color-block" :style="{ 'background-color': color }"></div>
    </div>
    <div class="subpage-hero__content-wrapper">
      <div class="subpage-hero__media">
        <img class="subpage-hero__image" v-if="image" :src="imageUrl" :alt="alt">
      </div>
      <div class="subpage-hero__content">
        <h1 class="subpage-hero__heading">{{ heading }}</h1>
        <div class="subpage-hero__span"></div>
        <p class="subpage-hero__description subpage-hero__description--last">{{ description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    color: String,
    image: String,
    alt: String,
    heading: String,
    description: String
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
.subpage-hero {
  min-height: calc(100vh - 70px);

  &__color-block-wrapper {
    display: none;
    grid-template-columns: 5% minmax(125px, 350px) 70%;
    position: absolute;
    width: 100vw;
    top: 0;
    // height: calc(100vh + 4.8rem);
    height: 100vh;
    max-width: 1200px;
    margin-left: auto; 
    margin-right: auto;
    left: 0;
    right: 0;

    @media only screen and (min-width: $desktop) {
      display: grid;
    }
  }

  &__color-block {
    grid-column: 2 / 3;
    background-color: $pop;
    display: none;

    @media only screen and (min-width: $desktop) {
      display: block;
    }
  }

  &__content-wrapper {
    background-color: $white; 
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    @media only screen and (min-width: $tablet) {
      flex-direction: row;
      @include mainContent();
    }
  }

  &__content {
    display: flex;
    flex-direction: column;
    align-items: center;

    @media only screen and (min-width: $tablet) {
      max-width: 50%;
      align-items: flex-start;
    }
  }

  &__heading {
    @include h1();
    margin-top: 1rem;
    margin-bottom: 1rem;
    font-size: 2rem;

    @media only screen and (min-width: $tablet) {
      font-size: 2rem;
    }

    @media only screen and (min-width: $desktop) {
      font-size: 3rem;
    }
  }

  &__media {
    z-index: 2;
    display: flex;
    justify-content: center
  }

  &__image {
    z-index: 1;
    margin-right: 2rem;
  }

  &__span {
    background: black;
    height: 1px;
    width: 50%;
    z-index: 1;
    margin-bottom: 1rem;

    @media only screen and (min-width: $desktop) {
      width: 150%;
      margin-left: -100%;
    }
  }

  &__description {
    margin: 0 .5rem 1rem .5rem;
    
    &--last {
      padding-bottom: 3rem;
    }
  }

  @media only screen and (min-width: $tablet) {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>