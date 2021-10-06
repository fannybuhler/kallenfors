<template>
  <div class="logo">
    <NuxtLink to="/">
      <img class="logo__image" src="@/assets/images/icons/kallenfors-logo.png" alt="Källenfors logotype">
    </NuxtLink>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.logo {
  position: absolute;
  align-self: center;
  z-index: 2;
  left: 10px;
  padding-top: 4px;
  width: 200px;

  @media only screen and (min-width: $desktop) {
    padding-top: 24px;
  }

  &__image {
    width: 80%;
    max-width: 160px;
  }
}

</style>