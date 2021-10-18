<template>
  <div class="carousel">
    <div class="carousel__media">
      <img class="carousel__image" :src="imageUrl" :alt="alt">
    </div>
    <div class="carousel__content" :class="dark ? 'dark' : ''">
      <div class="carousel__text">
        <h3 class="carousel__heading">{{ heading }}</h3>
        <p class="carousel__leading">{{ leading }}</p>
        <button class="carousel__button">
          <NuxtLink :to="link">{{ name }}s arbete</NuxtLink>
        </button>
      </div>
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
    name: String,
    dark: Boolean
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
  position: relative;

  &__image {
    width: 100%;
    max-height: 80vh;
    min-height: 50vh;
    object-fit: cover;
    display: block;
  }

  &__content {
    position: absolute;
    color: #fff;
    left: 0;
    bottom: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
  }

  .dark {
    color: #000;
  }

  &__text {
    width: 90%;

    @media only screen and (min-width: $tablet) {
      width: 40%;
    }
  }

  &__heading {
    @include h2();
    text-transform: none;
    text-shadow: 4px 4px 10px rgba(0, 0, 0, 0.4);
  }

  &__leading {
    font-size: 12px;
    text-shadow: 4px 4px 10px rgba(0, 0, 0, 0.4);
    margin-top: 10px;
    margin-bottom: 15px;

    @media only screen and (min-width: $tablet) {
      font-size: 16px;
      line-height: 160%;
    }
  }

  &__button {
    background: $pop;
    border: none;
    width: fit-content;
    padding: 8px 12px;
    text-transform: uppercase;
    font-weight: 400;
    letter-spacing: 2px;
    color: #000;
    margin: 10px 0;
    transition: 0.3s;

    &:hover {
      background: $darkpop;
    }

    @media only screen and (min-width: $tablet) {
      padding: 10px 15px;
      letter-spacing: 4px;
    }
  }

  a {
    text-decoration: none;
    color: #000;
    font-size: 10px;

    @media only screen and (min-width: $tablet) {
      font-size: 14px;
    }
  }
}
</style>