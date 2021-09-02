<template>
  <nav class="navbar">
    <ul class="navbar__list">
      <li>
        <NuxtLink to="/">Hem</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/juridik">Juridik</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/styrelsearbete">Styrelsearbete</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/marknadsforing">Marknadsföring</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/interimsuppdrag">Interimsuppdrag</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/kontakt">Kontakt</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
.navbar {
  font-size: 18px;
  display: flex;
  justify-content: center;
  padding-top: 36px;
  background: $white;

  &__list {
    display: flex;
    list-style: none;
    z-index: 1;
  }
}

a {
  text-decoration: none;
  margin: 0 1.5rem;
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
    height: 0.08em;
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
