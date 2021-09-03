<template>
  <div>
    <div class="landingPage">
      <!-- <div class="landingPage__color-block"></div> -->
      <img src="~/assets/images/photos/landingpage.png" alt="">
      <h1 class="landingPage__heading">Källenfors</h1>
      <h3 class="landingPage__subheading">Law & Consulting</h3>
    </div>
    <AboutUs />
    <Competence />
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.landingPage {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: $white; 

  &__color-block {
    height: 119%;
    width: 19rem;
    position: absolute;
    background-color: #F8BD59;
    top: 0;
    left: 11rem;
  }

  &__heading {
    text-transform: uppercase;
    font-weight: 400;
    font-size: 2rem;
    margin: .5rem 0;
    z-index: 1;
  }

  &__subheading {
    font-family: 'Playfair regular', serif;
    font-size: 1rem;
    font-weight: 200;
    padding-bottom: 10rem;
    z-index: 1;
  }
}
</style>
