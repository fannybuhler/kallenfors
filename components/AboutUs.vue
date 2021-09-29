<template>
  <div class="about">
    <h3 class="about__heading">VÅRT ARBETE</h3>
    <p class="about__body">Vi önskar få en nära relation till våra kunder. 
      Detta gynnar både vårt arbete och kundens möjlighet att få snabb och kostnadseffektiv hjälp, 
      eftersom vi känner varandra. Ingen startsträcka. Vi åtar oss att granska alla kommersiella 
      relationer som kundens bolag har ur ett legalt riskperspektiv – vilka relationer det än är. 
    </p>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.about {
  @include blockPadding();
  @include mainContent();

  &__heading {
    font-family: 'Playfair regular';
    font-size: 32px;
    line-height: 160%;
    font-weight: 300;
    position: relative;
  }

  &__body {
    font-size: 16px;
    line-height: 160%;
  }
  
  @media only screen and (min-width: $tablet) {
    .about {
      &__heading {
        font-size: 48px;
      }
      
      &__body {
        margin-right: 20%;
        font-size: 24px;
      }
    }
  }
}
</style>