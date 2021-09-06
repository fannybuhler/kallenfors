<template>
  <div>
    <div class="landing-page">
      <div class="landing-page__color-block"></div>
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
  height: calc(100vh - 50px);
  display: flex;
  flex-direction: column;
  justify-content: center;
  background-color: $white; 

  &__color-block {
    height: 109.5%;
    width: 9rem;
    position: absolute;
    background-color: $pop;
    top: 0;
    left: 2rem;
  }

  &__image {
    z-index: 1;
    margin: 10px 50px;
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
    margin: 0 0 5px 50px;
    z-index: 1;
  }

  &__subheading {
    font-family: 'Montserrat';
    text-transform: uppercase;
    font-size: 1.5rem;
    font-weight: 200;
    margin: 5px 0 0 50px;
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
