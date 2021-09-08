<template>
  <div class="landing-page">
    <div class="landing-page__color-block-wrapper">
      <div class="landing-page__color-block"></div>
    </div>
    <div class="landing-page__content-wrapper">
      <h1 class="landing-page__heading">Peter <br> & <br> Anna-Karin <br> Källenfors</h1>
      <img class="landing-page__image" src="~/assets/images/photos/landingpage-big.png" alt="corporate photo of lawyers">
      <h3 class="landing-page__subheading">Law & <br> Consulting</h3>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.landing-page {
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

  &__content-wrapper {
    background-color: $white; 
    height: calc(100vh - 70px);
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-left: 15%;
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

  &__image {
    z-index: 1;
    margin-top: 10px;
    width: 70%;
    max-width: 350px;
    box-shadow: 0px 35px 25px -25px rgba(0, 0, 0, 0.25);
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
      bottom: calc(100vh - 93vh);
      left: 0;
      height: 1px;
      width: 70%;
      max-width: 600px;
    }
  }

  @media only screen and (min-width: $tablet) {
    .landing-page {
      &__content-wrapper {
        display: grid;
        grid-template-columns: repeat(12, 1fr);
        grid-template-rows: 1fr 1fr 35%;
        padding-left: 0;
      }

      &__image {
        grid-column: 2   / 6;
        grid-row: 2 / 3;
        width: fit-content;
      }

      &__heading {
        grid-column: 8 / 12;
        grid-row: 2 / 3;
        align-self: center;
        margin: 0;

        &__and {
          display: block;
        }
      }

      &__subheading {
        grid-column: 8 / 12;
        grid-row: 2 / 3;
        padding-bottom: 0;
        align-self: end;
        margin: 0;
      }
    }
  }

  
}
</style>