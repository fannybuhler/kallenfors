<template>
  <div class="navbar-wrapper">
    <ul class="navbar-wrapper__list">
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
        <NuxtLink to="/terapihundar">Andra engagemang</NuxtLink>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.navbar-wrapper {
  font-size: 18px;
  display: flex;
  justify-content: flex-end;
  padding: 30px 0 8px 0;
  background: $white;

  &__list {
    display: flex;
    list-style: none;
    z-index: 1;
    margin: 0;
  }

  &__list-item {
    margin: 0.5rem 0;
  }
}

a {
  text-decoration: none;
  margin: 0 1rem;
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

@media only screen and (max-width: $desktop - 1px) {
  .navbar-wrapper {
    display: none;
  }
}
</style>