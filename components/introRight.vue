<template>
  <div class="intro-right">
    <div class="intro-right__color-block"></div>
    <img class="intro-right__image" src="@/assets/images/photos/anna-karin.jpeg" alt="Porträttfoto av Anna-Karin Källenfors avslappnat klädd">
    <h3 class="intro-right__heading">I dagens brus krävs en grundlig och noggrann planering för marknadsföringen.</h3>
    <div class="intro-right__span"></div>
    <p class="intro-right__body">Anna-Karin Källenfors har 15 års erfarenhet av att projektledning, 
      kampanjutveckling och digitala kommunikationsstrategier. 
      Anna-Karin arbetar även regelbundet med löpande marknadsstöd och uppföljning.
    </p>
  </div>
</template>

<style lang="scss" scoped>
.intro-right {
  margin: 3rem 0;
  position: relative;

  &__color-block {
    height: 140px;
    width: 90%;
    background-color: $pop;
    position: absolute;
    top: 115px;
    right: 0;
    z-index: -1;
  }

  &__image {
    height: 70%;
    width: 70%;
    margin-right: 10%;
    z-index: 1;
    float: right;
    margin-right: 10%;
    max-height: 724px;
    max-width: 550px;
  }

  &__heading {
    font-size: 26px;
    margin: 10px 20px;
    text-transform: uppercase;
    clear: right;
    padding-top: 20px;
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