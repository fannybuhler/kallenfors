<template>
  <div class="intro-right">
    <div class="intro-right__image-wrapper">
      <div class="intro-right__color-block"></div>
      <img class="intro-right__image" src="@/assets/images/photos/anna-karin.jpeg" alt="Porträttfoto av Anna-Karin Källenfors avslappnat klädd">
    </div>
    <div class="intro-right__content-wrapper">
      <h3 class="intro-right__heading">I dagens brus krävs en grundlig och noggrann planering för marknadsföringen.</h3>
      <div class="intro-right__span"></div>
      <p class="intro-right__body">Anna-Karin Källenfors har 15 års erfarenhet av att projektledning, 
        kampanjutveckling och digitala kommunikationsstrategier. 
        Anna-Karin arbetar även regelbundet med löpande marknadsstöd och uppföljning.
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.intro-right {
  margin: 3rem 0;
  padding-top: 3rem;
  display: flex;
  flex-direction: row-reverse;
  flex-wrap: wrap;

  &__image-wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
  }

  &__color-block {
    width: 85%;
    background-color: #F8BD59;
    z-index: -1;
    grid-column: 1 / 4;
    grid-row: 2 / 3;
    justify-self: end;
  }

  &__image {
    height: auto;
    width: 70%;
    margin-right: -12%;
    z-index: 1;
    max-height: 724px;
    max-width: 550px;
    grid-column: 1 / 4;
    justify-self: center;
    align-self: center;
    grid-row: 1 / 4;
  }

  &__heading {
    font-size: 26px;
    margin: 10px 20px;
    text-transform: uppercase;
  }
  
  &__span {
    background: black;
    height: 1px;
    width: 30%;
    margin: 20px 20px;
  }

  &__body {
    margin: 0 20px;
  }

  @media only screen and (min-width: $tablet) {
    .intro-right {
      &__image-wrapper {
        width: 50%;
      }

      &__content-wrapper {
        width: 50%;
        align-self: center;
      }

      &__color-block {
        width: 100%;
      }

      &__heading {
        font-size: 33px;
      }

      &__span {
        margin-right: -15%;
      }
      
      &__body {
        font-size: 22px;
      }
    }
  }
}
</style>