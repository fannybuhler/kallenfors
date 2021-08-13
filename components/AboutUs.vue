<template>
  <div class="about">
    <h3 class="about__heading">Om oss</h3>
    <p class="about__body">Vi önskar få en nära relation till våra kunder. 
      Detta gynnar både vårt arbete och kundens möjlighet att få snabb och kostnadseffektiv hjälp, 
      eftersom vi känner varandra. Ingen startsträcka. Vi åtar oss att granska alla kommersiella 
      relationer som kundens bolag har ur ett legalt riskperspektiv – vilka relationer det än är. 
      I övrigt tror vi att vi kan hjälpa till med bolagets egen struktur med hjälp att ordna 
      dokumentation kring styrelsearbetet, ledningsfrågor, bolagsordningar och förberedelser 
      och genomförandet av bolagsstämmor.
    </p>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.about {
  background: $beige;
  max-width: 1200px;
  margin: 0 auto;
  padding: 5rem 2rem;

  &__heading {
    font-family: 'Playfair regular';
    font-size: 32px;
  }

  &__body {
    font-size: 18px;
    line-height: 160%;
  } 
}
</style>