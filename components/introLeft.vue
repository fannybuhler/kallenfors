<template>
  <div class="intro-left">
    <div class="intro-left__color-block"></div>
    <img class="intro-left__image" src="@/assets/images/photos/peter.jpeg" alt="Porträttfoto av Peter Källenfors avslappnat klädd">
    <h3 class="intro-left__heading">25 års erfarenhet av att leverera juridik på en hög kvalitativ nivå.</h3>
    <div class="intro-left__span"></div>
    <p class="intro-left__body">Peter Källenfors har mångårig erfarenhet av att lämna rådgivning vid x, y  och z
       samt i bolagsrättsliga frågor. Peter arbetar även regelbundet med alla typer av 
       kommersiella tvister och i skiljeförfaranden.</p>
  </div>
</template>

<style lang="scss" scoped>
.intro-left {
  margin-top: 2rem;
  position: relative;

  &__color-block {
    height: 140px;
    width: 90%;
    background-color: $pop;
    position: absolute;
    top: 95px;
    z-index: -1;
  }

  &__image {
    height: 70%;
    width: 70%;
    margin-left: 10%;
    z-index: 1;
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
}

</style>