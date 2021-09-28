<template>
  <div class="person-hero">
    <div class="person-hero__color-block-wrapper">
      <div class="person-hero__color-block"></div>
    </div>
    <div class="person-hero__content">
      <img class="person-hero__image" v-if="image" :src="require(`@/assets/images/${image}`)" :alt="alt">
      <h1 class="person-hero__heading">{{ heading }}</h1>
      <p class="person-hero__leading">{{ role }}</p>
      <p class="person-hero__leading">{{ location }}</p>
      <p class="person-hero__leading">{{ phone }}</p>
      <p class="person-hero__leading">{{ mail }}</p>
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
    location: String,
    phone: String,
    mail: String,
  },
}
</script>

<style lang="scss" scoped>
.person-hero {
  @include boxer(red, 0, 2);
  display: flex;
  height: 100vh;

  &__color-block-wrapper {
    display: grid;
    grid-template-columns: 5% minmax(125px, 350px) 70%;
    position: absolute;
    width: 100vw;
    top: 0;
    height: calc(100vh + 3.8rem);
    max-width: 1200px;
    margin-left: auto; 
    margin-right: auto;
    left: 0;
    right: 0;
  }

  &__color-block {
    grid-column: 2 / 3;
    background-color: $pop;
  }

  &__media {
    //
  }

  &__image {
    z-index: 1;
    margin-top: 10px;
    width: 70%;
    max-width: 350px;
    box-shadow: 0px 35px 25px -25px rgba(0, 0, 0, 0.25);
  }

  &__content {
    background-color: $white; 
    height: calc(100vh - 70px);
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-left: 15%;
  }

  &__heading {
    //
  }

  &__leading {
    //
  }


}

</style>