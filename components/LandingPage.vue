<template>
  <div class="landing-page">
    <div class="landing-page__color-block-wrapper">
      <div class="landing-page__color-block"></div>
    </div>
    <div class="landing-page__content-wrapper">
      <h1 class="landing-page__heading">Peter <br> & <br> Anna-Karin <br> Källenfors</h1>
      <div class="landing-page__media">
        <img class="landing-page__image" src="~/assets/images/photos/kallenfors.jpg" alt="corporate photo of lawyers">
      </div>
      <h2 class="landing-page__subheading">Law & <br> Consulting</h2>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.landing-page {
  background: $white;
  height: calc(100vh - 70px);
  display: flex;

  &__color-block-wrapper {
    @include pageWrap();
    display: grid;
    grid-template-columns: 5% minmax(125px, 350px) 70%;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 100%;
    width: 100%;
    // width: 100vw;
    // min-height: 100vh;
    // max-width: 1200px;
    // margin-left: auto; 
    // margin-right: auto;
  }

  &__color-block {
    grid-column: 2 / 3;
    background-color: $pop;
  }

  &__content-wrapper {
    @include pageWrap();
    background-color: $white;
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
    font-weight: 400;
    margin-top: 5%;
    margin-bottom: 5px;
    z-index: 1;
  }

  &__media {
    z-index: 1;
    margin-top: 10px;
    max-width: 80%;
  }

  &__image {
    width: 100%;
    height: 100%;
    display: block;
  }

  &__subheading {
    font-family: 'Montserrat';
    text-transform: uppercase;
    font-size: 1.5rem;
    font-weight: 200;
    margin-top: 10px;
    z-index: 1;
    padding-bottom: 70px;
  }

  @media only screen and (min-width: $tablet) {
    .landing-page {
      &__content-wrapper {
        height: 100%;
        width: 100%;
        display: grid;
        grid-template-columns: repeat(12, 1fr);
        grid-template-rows: 1fr 1fr 1fr;
        grid-gap: 25px;
        padding-left: 0;
      }

      &__media {
        grid-column: 2 / 8;
        grid-row: 2 / 3;
        align-self: end;
        justify-self: end;
      }

      &__heading {
        grid-column: 8 / 12;
        grid-row: 2 / 3;
        align-self: center;
        margin: 0;
        font-size: 2.2rem;
      }

      &__subheading {
        grid-column: 8 / 12;
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
      &__heading {
        font-size: 3.3rem;
      }

      &__subheading {
        font-size: 2rem;
        line-height: 100%;
      }

      &__span {
        margin-top: 5%;
      }
    }
  }

  
}
</style>