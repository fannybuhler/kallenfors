<template>
  <div>
    Anna-Karin Källenfors
    <br>
    <PromoCards
      heading="Erfarenhet"
      :items="items"
    />
  </div>
</template>

<script>
import items from '@/data/experience-ak'

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
