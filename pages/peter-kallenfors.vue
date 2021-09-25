<template>
  <div>
    Peter Källenfors
    <br>
    <PromoCards
      heading="My heading"
      :items="items"
    />
  </div>
</template>

<script>
import items from '@/data/experience'

export default {
  data () {
    return {
      items
    }
  }
}
</script>

<style>

</style>
