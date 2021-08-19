<template>
  <div>
    <div class="landingPage">
      <div class="landingPage__circle"></div>
      <h1 class="landingPage__heading">Källenfors</h1>
      <h3 class="landingPage__subheading">Law & Consulting</h3>
      <div class="socialMedia">
        <img class="socialMedia__logo" src="~/assets/images/instalogo.png" />
        <img class="socialMedia__logo" src="~/assets/images/linkedinlogo.png" />
      </div>
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
  height: 92vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: $white; /* Needed for mix-blend-mode */
  isolation: isolate; /* Without isolation, the background color will be taken into account */

  &__circle {
    height: 144px;
    width: 144px;
    border-radius: 50%;
    background-color: $white;
    mix-blend-mode: difference;
    position: relative;
    top: 4rem;
    left: 11rem;
  }

  &__heading {
    text-transform: uppercase;
    font-weight: 400;
    font-size: 4.5rem;
    margin: .5rem 0;
  }

  &__subheading {
    font-family: 'Playfair regular', serif;
    font-size: 1.5rem;
    font-weight: 200;
    padding-bottom: 10rem;
  }
}

.socialMedia {
  position: absolute;
  left: 5px;

  &__logo {
    max-height: 42px;
    display: block;
    margin: .5rem;
  }
}
</style>
