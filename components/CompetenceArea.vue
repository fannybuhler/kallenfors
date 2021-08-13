<template>
  <div class="competenceArea dummy">
    <img class="competenceArea__icon" src="~/assets/images/handshake.png" alt="vector icon of handshake">
    <div>
      <h3 class="competenceArea__heading">Affärsjuridik</h3>
      <span class="competenceArea__span"></span>
      <p class="competenceArea__body">Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.dummy {
  border: 2px dotted red;
  background: rgb(255, 235, 235);
  margin: 5px;
}
.competenceArea {
  display: flex;

  &__icon {
    border: 1px solid black;
    border-radius: 50%;
  }

  &__heading {

  }

  &__span {
    background: $black;
    color: $black;
  }

  &__body {

  }
}
</style>