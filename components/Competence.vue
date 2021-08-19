<template>
  <div class="expertise">
    <h3 class="expertise__heading">Kompetensområden</h3>
    <div class="expertise__wrapper">
      <CompetenceArea 
        title="Affärsjuridik" 
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit"
        imageUrl="handshake.png"
      />
      <CompetenceArea 
        title="Bolagsrätt" 
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit"
        imageUrl="risk.png"
      />
      <CompetenceArea 
        title="Komersiella avtal"  
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit"
        imageUrl="agreement.png"
      />
      <CompetenceArea 
        title="Tvistelösning" 
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit"
        imageUrl="hammer.png"
      />
      <CompetenceArea 
        title="Styrelsearbete" 
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit"
        imageUrl="suitcase.png"
      />
      <CompetenceArea 
        title="Marknadsföring" 
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit"
        imageUrl="seo.png"
      />
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.expertise {
  background: $white;

  &__heading {
    display: flex;
    justify-content: center;
    padding: 5rem 0 2rem 0;
    font-family: 'Playfair regular';
    font-weight: 200;
    font-size: 32px;
  }

  &__wrapper {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    padding-bottom: 5rem;
  }
}
</style>