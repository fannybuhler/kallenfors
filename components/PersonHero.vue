<template>
  <div class="person-hero">
    <div class="person-hero__color-block-wrapper">
      <div class="person-hero__color-block"></div>
    </div>
    <div class="person-hero__content-wrapper">
      <div class="person-hero__media">
        <img class="person-hero__image" v-if="image" :src="require(`@/assets/images/${image}`)" :alt="alt">
      </div>
      <div class="person-hero__content">
        <h1 class="person-hero__heading">{{ heading }}</h1>
        <p class="person-hero__leading">{{ role }}</p>
        <p class="person-hero__leading person-hero__location">
          <img class="person-hero__icon" src="@/assets/images/icons/map-pin.png" alt="map pin incon" />
          <span v-for="location, index in location" :key="index" v-text="location" class="person-hero__tag"></span>
        </p>
        <p class="person-hero__leading">Telefon <span>{{ phone }}</span></p>
        <p class="person-hero__leading--last">Mail <span>{{ mail }}</span></p>
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

  // @include boxer(red);

  // &__color-block-wrapper {
  //   display: grid;
  //   grid-template-columns: 5% minmax(125px, 350px) 70%;
  //   position: absolute;
  //   width: 100vw;
  //   top: 0;
  //   height: calc(100vh + 3.8rem);
  //   max-width: 1200px;
  //   margin-left: auto; 
  //   margin-right: auto;
  //   left: 0;
  //   right: 0;
  // }

  // &__color-block {
  //   grid-column: 2 / 3;
  //   background-color: $pop;
  // }

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
  }

  &__image {
    z-index: 1;
    width: 100%;
    max-width: 450px;
  }
  
  &__icon {
    display: inline;
    width: 20px;
  }

  &__tag {
    margin: 0 3px;
  }

  &__leading {
    margin: .5rem;
    
    &--last {
      padding-bottom: 3rem;
    }
  }

  &__location {
    display: flex;
    align-items: center;
  }

  @media only screen and (min-width: $tablet) {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>