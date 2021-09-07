<template>
  <div>
      <div class="landing-page__color-block-wrapper">
        <div class="landing-page__color-block"></div>
      </div>
    <div class="landing-page">
      <h1 class="landing-page__heading">Peter & <br> Anna-Karin <br> Källenfors</h1>
      <img class="landing-page__image" src="~/assets/images/photos/landingpage.png" alt="corporate photo of lawyers">
      <h3 class="landing-page__subheading">Law & <br> Consulting</h3>
    </div>
    <AboutUs />
    <IntroLeft />
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.landing-page {
  background-color: $white; 
  height: calc(100vh - 50px);
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-left: 15%;

  &__color-block-wrapper {
    display: grid;
    grid-template-columns: 19px minmax(125px, 350px) 70%;
    position: absolute;
    width: 100vw;
    top: 0;
    height: calc(100vh + 4rem);
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

  &__image {
    z-index: 1;
    margin-top: 10px;
    height: 256px;
    width: 256px;
    box-shadow: 0px 35px 25px -25px rgba(0, 0, 0, 0.25);
  }

  &__heading {
    font-family: 'Playfair regular';
    font-size: 2.3rem;
    text-transform: uppercase;
    line-height: 100%;
    font-weight: 600;
    margin-bottom: 5px;
    z-index: 1;
  }

  &__subheading {
    font-family: 'Montserrat';
    text-transform: uppercase;
    font-size: 1.5rem;
    font-weight: 200;
    margin-top: 5px;
    z-index: 1;
    padding-bottom: 70px;

    &:after {
      content: "";
      background: black;
      position: absolute;
      bottom: 12%;
      left: 0;
      height: 1px;
      width: 70%;
    }
  }
}
</style>
