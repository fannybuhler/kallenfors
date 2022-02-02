<template>
  <div class="landing-page">
    <div class="landing-page__pagewrap">
      <div class="landing-page__colorblock">
        <div class="landing-page__colorblock-block"></div>
      </div>
      <div class="landing-page__content">
        <h1 class="landing-page__heading">Peter <br> & <br> Anna-Karin <br> Källenfors</h1>
        <img class="landing-page__image" src="~/assets/images/photos/kallenfors.jpg" alt="corporate photo of lawyers">
        <h2 class="landing-page__subheading">Law & <br> Consulting</h2>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.landing-page {
  @include boxer();
  background: $white;

  &__pagewrap {
    @include pageWrap();
  }

  &__colorblock {

  }

  &__colorblock-block {

  }

  &__content {

  }

  &__heading {

  }

  &__image {

  }

  &__subheading {

  }
}
</style>