<template>
  <div class="about">
    <h3 class="about__heading">OM BOLAGET</h3>
    <p class="about__body">
      Källenfors Law & Consulting AB är ett konsultbolag som ägs och drivs av Peter och Anna-Karin Källenfors. Bolaget tillhandahåller tjänster inom juridik, marknadsföring, rekrytering och managementfrågor. Bolaget verkar i både Stockholm och Sundsvall.
    </p>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.about {
  @include mainContent();
  padding-top: 3rem;

  @media only screen and (min-width: $desktop) {
    padding-top: 4rem;
  }

  &__heading {
    font-family: 'Playfair regular';
    font-size: 32px;
    line-height: 160%;
    font-weight: 400;
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