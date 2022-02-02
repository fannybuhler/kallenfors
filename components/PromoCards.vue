<template>
  <div class="promo-cards">
    <h2 v-if="heading" class="promo-cards__heading" v-text="heading" />
    <div class="promo-cards__span"></div>
    <div class="promo-cards__list">
      <div v-for="item, index in items" :key="index" class="promo-cards__item">
        <PromoCard
          :heading="item.heading"
          :leading="item.leading"
          :image="item.image"
          :tags="item.tags"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    heading: {
      type: String,
      default: ''
    },
    items: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style lang="scss" scoped>
.promo-cards {
  @include pageWrap();
  @include mainContent();
  @include blockPadding();

  &__heading {
    @include h2();
    // margin-bottom: 1rem;
  }

  &__list {
    display: grid;
    grid-gap: 3rem;

    @media only screen and (min-width: $tablet) {
      display: grid;
      grid-gap: 3rem 1.5rem;
      grid-template-columns: repeat(2, 1fr);
    }

    @media only screen and (min-width: $desktop) {
      grid-template-columns: repeat(3, 1fr);
    }
  }

  &__span {
    background: black;
    height: 1px;
    width: 70%;
    margin-top: 1rem;
    margin-bottom: 1.5rem;
    position: relative;
    left: -5%;

    @media only screen and (min-width: $tablet) {
      margin-top: 1.5rem;
      margin-bottom: 2rem;
      width: 50%;
    }
  }
}
</style>
