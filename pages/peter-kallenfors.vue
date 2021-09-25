<template>
  <div>
    Peter Källenfors
    <br>
    <PromoCards
      heading="Erfarenhet"
      :items="items"
    />
  </div>
</template>

<script>
import items from '@/data/experience-peter'

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
