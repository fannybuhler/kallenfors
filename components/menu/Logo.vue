<template>
  <div class="logo">
    <img class="logo__image" src="@/assets/images/icons/kallenfors-logo.png" alt="Källenfors logotype">
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
  padding-top: 30px;
  width: 200px;

  &__image {
    width: 80%;
    max-width: 160px;
  }
}

</style>