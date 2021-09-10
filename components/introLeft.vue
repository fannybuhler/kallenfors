<template>
  <div class="intro-left intro-left__wrapper">
    <div class="intro-left__image-wrapper">
      <div class="intro-left__color-block"></div>
      <img class="intro-left__image" src="@/assets/images/photos/peter.jpeg" alt="Porträttfoto av Peter Källenfors avslappnat klädd">
    </div>
    <div class="intro-left__content-wrapper">
      <h3 class="intro-left__heading">25 års erfarenhet av att leverera juridik på en hög kvalitativ nivå.</h3>
      <div class="intro-left__span"></div>
      <p class="intro-left__body">Peter Källenfors har mångårig erfarenhet av att lämna rådgivning vid x, y  och z
        samt i bolagsrättsliga frågor. Peter arbetar även regelbundet med alla typer av 
        kommersiella tvister och i skiljeförfaranden.
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.intro-left {
  margin: 3rem 0;
  padding-top: 3rem;
  display: flex;
  flex-direction: row;
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
  }

  &__image {
    height: auto;
    width: 70%;
    margin-left: -12%;
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
    .intro-left {
      &__image-wrapper {
        width: 50%;
        align-self: center;
      }

      &__content-wrapper {
        width: 50%;
      }
    }
  }
}

</style>