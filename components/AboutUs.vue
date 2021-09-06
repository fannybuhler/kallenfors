<template>
  <div class="about">
    <h3 class="about__heading" ref="heading" @click=getPos(this)>VÅRT ARBETE</h3>
    <p class="about__body">Vi önskar få en nära relation till våra kunder. 
      Detta gynnar både vårt arbete och kundens möjlighet att få snabb och kostnadseffektiv hjälp, 
      eftersom vi känner varandra. Ingen startsträcka. Vi åtar oss att granska alla kommersiella 
      relationer som kundens bolag har ur ett legalt riskperspektiv – vilka relationer det än är. 
    </p>
  </div>
</template>

<script>
export default {
  methods: {
    getPos(heading) {
      const top = this.$refs.heading.getBoundingClientRect().top
      console.log('top:', top)
    }
  }
}
</script>

<style lang="scss" scoped>
.about {
  background: $beige;
  max-width: 1200px;
  margin: 0 auto;
  padding: 1rem 2rem;

  &__heading {
    font-family: 'Playfair regular';
    font-size: 32px;
    font-weight: 300;
    position: relative;
  }

  &__body {
    font-size: 18px;
    line-height: 160%;
  } 
}
</style>