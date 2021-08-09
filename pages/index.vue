<template>
  <div class="landingPage">
    <h1 class="landingPage__heading">Källenfors</h1>
    <h3 class="landingPage__subheading">Law & Consulting</h3>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.landingPage {
  height: 80vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  &__heading {
    text-transform: uppercase;
    font-weight: 200;
    font-size: 4rem;
    margin: .5rem 0;
  }

  &__subheading {
    font-family: 'Playfair regular', serif;
    font-size: 1.5rem;
  }
}
</style>
