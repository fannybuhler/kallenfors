<template>
  <header class="landing-page">
    <div class="landing-page__color-block-wrapper">
      <div class="landing-page__color-block"></div>
    </div>
    <div class="landing-page__content-wrapper">
      <h1 class="landing-page__heading">Peter <br> & <br> Anna-Karin <br> Källenfors</h1>
      <img class="landing-page__image" src="~/assets/images/photos/landingpage-big.png" alt="corporate photo of lawyers">
      <h3 class="landing-page__subheading">Law & <br> Consulting</h3>
      <div class="landing-page__span"></div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.landing-page {
  &__color-block-wrapper {
    display: grid;
    grid-template-columns: 5% minmax(125px, 350px) 70%;
    position: absolute;
    width: 100vw;
    top: 0;
    height: calc(100vh + 4.8rem);
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
    max-width: 300px;
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
      bottom: calc(100vh - 92vh);
      left: 0;
      height: 1px;
      width: 70%;
      max-width: 600px;
    }
  }

  

  @media only screen and (min-width: $tablet) {
    .landing-page {
      &__color-block-wrapper {
        height: calc(100vh + 5.55rem);
      }

      &__content-wrapper {
        display: grid;
        grid-template-columns: repeat(12, 1fr);
        grid-template-rows: 0.5fr 1fr 1fr;
        grid-gap: 25px;
        padding-left: 0;
      }

      &__image {
        grid-column: 2 / 7;
        grid-row: 2 / 3;
        max-width: 450px;
        object-fit: cover;
        width: 100%;
        max-height: 100%;
      }

      &__heading {
        grid-column: 7 / 12;
        grid-row: 2 / 3;
        align-self: center;
        margin: 0;
        font-size: 2.2rem;
      }

      &__subheading {
        grid-column: 7 / 12;
        grid-row: 2 / 3;
        padding-bottom: 0;
        align-self: end;
        margin: 0;
        margin-bottom: -5px;

        &:after {
          display: none;
        }
      }

      &__span {
        background: black;
        height: 1px;
        width: 100%;
        grid-column: 1 / 8;
        grid-row: 3;
        z-index: 1;
        align-self: start;
        margin-top: 1rem;
      }
    }
  }

  @media only screen and (min-width: $desktop) {
    .landing-page {
      // &__image {
      //   max-width: 620px;
      // }

      &__heading {
        font-size: 3.3rem;
      }

      &__subheading {
        font-size: 1.5rem;
      }

      &__span {
        margin-top: 5%;
      }
    }
  }

  
}
</style>