<template>
  <div class="competence">
    <img class="competence__icon" :src="{imageUrl}" />
    <div class="competence__text-wrapper">
      <h3 class="competence__heading">{{ title }}</h3>
      <div class="competence__span"></div>
      <p class="competence__body">{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    description: String,
    imageUrl: String,
 }
}
</script>

<style lang="scss" scoped>
// .dummy {
//   border: 2px dotted red;
//   background: rgb(255, 235, 235);
//   margin: 5px;
// }
.competence {
  display: flex;
  width: fit-content;
  margin: 1rem;
  align-items: center;
  justify-content: center;

  &__text-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  &__icon {
    border: 1px solid black;
    border-radius: 50%;
    margin-right: 1rem;
    height: 64px;
    width: 64px;
    padding: 15px;
  }

  &__heading {
    font-family: 'Playfair regular';
    font-weight: 200;
    font-size: 22px;
    margin: .5rem 0 .5rem 0;
  }

  &__span {
    background: $black;
    color: $black;
    height: 2px;
    width: 25px;
  }

  &__body {
    font-size: 12px;
    word-break: 5;
  }
}
</style>