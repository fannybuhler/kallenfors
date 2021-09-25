<template>
  <div class="promo-cards">
    <h2 v-if="heading" class="promo-cards" v-text="heading" />
    <div v-for="item, index in items" :key="index">
      item: {{ index }} {{ item.heading }}
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
  @include boxer(red);
}
</style>
