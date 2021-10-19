<template>
  <div class="person-hero">
    <div class="person-hero__color-block-wrapper">
      <div class="person-hero__color-block"></div>
    </div>
    <div class="person-hero__content-wrapper">
      <div class="person-hero__media">
        <img class="person-hero__image" v-if="image" :src="require(`@/assets/images/${image}`)" :alt="alt">
        <div class="person-hero__overlay"></div>
      </div>
      <div class="person-hero__content">
        <h1 class="person-hero__heading">{{ heading }}</h1>
        <p class="person-hero__leading person-hero__leading--bold">{{ role }}</p>
        <p class="person-hero__leading person-hero__location">
          <img class="person-hero__icon" src="@/assets/images/icons/map-pin.png" alt="map pin incon" />
          <span v-for="location, index in location" :key="index" v-text="location" class="person-hero__tag"></span>
        </p>
        <div class="person-hero__span"></div>
        <div class="person-hero__contact">
          <span class="person-hero__leading person-hero__leading--fade">Telefon</span>
          <span class="person-hero__leading">{{ phone }}</span>
          <span class="person-hero__leading person-hero__leading--last person-hero__leading--fade">Mail</span>
          <span class="person-hero__leading">{{ mail }}</span>
        </div>
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
    role: String,
    location: Array,
    phone: String,
    mail: String,
  },
}
</script>

<style lang="scss" scoped>
.person-hero {
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
    }
  }

  &__content {
    display: flex;
    flex-direction: column;
    align-items: center;

    @media only screen and (min-width: $tablet) {
      max-width: 50%;
    }
  }

  &__heading {
    @include h1();
    margin: 1rem;

    @media only screen and (min-width: $tablet) {
      font-size: 3.5rem
    }
  }

  &__media {
    position: relative;
  }

  &__image {
    width: 100%;
    max-width: 450px;
  }

  &__overlay {
    color: #fff;
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 98.5%;
    text-align: center;
    background: linear-gradient(180deg, rgba(0, 0, 0, 0.4) 0%, rgba(0, 0, 0, 0) 24.85%, rgba(0, 0, 0, 0) 75.42%, rgba(0, 0, 0, 0.4) 100%);
  }
  
  &__icon {
    display: inline;
    width: 20px;
  }

  &__location {
    display: flex;
    align-items: center;
  }

  &__tag {
    margin: 0 3px;
  }

  &__span {
    background: black;
    height: 1px;
    width: 50%;
    z-index: 1;
    margin-bottom: 1rem;

    // @media only screen and (min-width: $desktop) {
    //   width: 150%;
    //   margin-left: -120%;
    // }
  }

  &__contact {
    display: grid;
    grid-column-gap: 1rem;
    grid-template-columns: auto auto;
    grid-template-rows: auto auto;

    @media only screen and (min-width: $tablet) {
      grid-column-gap: 2.5rem;
    }
  }

  &__leading {
    margin: 0 .5rem 1rem .5rem;
    
    &--last {
      padding-bottom: 3rem;
    }
    
    &--bold {
      font-weight: 600;
    }

    &--fade {
      color: #696969;
    }
  }


  @media only screen and (min-width: $tablet) {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>