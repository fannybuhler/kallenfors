<template>
  <div class="navbar">
    <NuxtLink to="/">Hem</NuxtLink>
    <NuxtLink to="/about">Om oss</NuxtLink>
    <NuxtLink to="/contact">Kontakt</NuxtLink>
    <NuxtLink to="/highlight">Interimsuppdrag</NuxtLink>
  </div>
</template>

<style lang="scss" scoped>
.navbar {
  font-size: 18px;
  display: flex;
  justify-content: center;
  margin-top: 36px;
}

a {
  text-decoration: none;
  margin: 0 2rem;
  display: block;
  position: relative;
  padding: 0.2em 0;
}

/* Underline animation */
a {
  &:link {
    color: $black;
  }

  &:visited {
    color: $black;
  }


  &:active {
    color: $black;
  }

  &:focus::after {
    transform: scale(1);
  }

  &:hover {
    color: $black;

    &::after {
      transform: scale(1);
    }
  }

  &::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 0.1em;
    background-color: $black;
    opacity: 0;
    transition: opacity 300ms, transform 300ms;
  }

  &::after {
    opacity: 1;
    transform: scale(0);
    transform-origin: center;
  }
}

</style>
<script>

</script>
