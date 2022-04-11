<template>
  <div class="navbar">
    <nav class="navbar__nav">
      <MenuLogo />
      <MenuBurger />
      <MenuSidebar>
        <ul class="navbar__list">
          <li
            class="navbar__list-item"
            @click="closeSidebarPanel"
            v-if="isPanelOpen"
          >
            <NuxtLink to="/">Hem</NuxtLink>
          </li>
          <li
            class="navbar__list-item"
            @click="closeSidebarPanel"
            v-if="isPanelOpen"
          >
            <NuxtLink to="/juridik">Juridik</NuxtLink>
          </li>
          <li
            class="navbar__list-item"
            @click="closeSidebarPanel"
            v-if="isPanelOpen"
          >
            <NuxtLink to="/styrelsearbete">Styrelsearbete</NuxtLink>
          </li>
          <li
            class="navbar__list-item"
            @click="closeSidebarPanel"
            v-if="isPanelOpen"
          >
            <NuxtLink to="/marknadsforing">Marknadsföring</NuxtLink>
          </li>
          <li
            class="navbar__list-item"
            @click="closeSidebarPanel"
            v-if="isPanelOpen"
          >
            <NuxtLink to="/interimsuppdrag">Interimsuppdrag</NuxtLink>
          </li>
          <li
            class="navbar__list-item"
            @click="closeSidebarPanel"
            v-if="isPanelOpen"
          >
            <NuxtLink to="/terapihundar">Terapihundar</NuxtLink>
          </li>
        </ul>
      </MenuSidebar>
      <MenuDesktop />
    </nav>
  </div>
</template>

<script>
import { store, mutations } from "@/store.js";
export default {
  computed: {
    isPanelOpen() {
      return store.isNavOpen;
    },
  },

  methods: {
    closeSidebarPanel: mutations.toggleNav,
  },
};
</script>

<style lang="scss" scoped>
.navbar {
  background: $white;

  &__nav {
    font-size: 18px;
    display: flex;
    justify-content: flex-end;
    background: $white;
  }

  &__list {
    list-style: none;
    padding: 0;
  }

  &__list-item {
    margin: 0.5rem 0;
  }
}

a {
  text-decoration: none;
  margin: 0 1.5rem;
  display: block;
  padding: 0.2em 0;
}

a:link,
a:visited,
a:active,
a:hover {
  color: $black;
}

@media only screen and (min-width: $desktop) {
  .navbar__nav {
    margin: 0 auto;
    position: relative;
    max-width: 1200px;
  }
}
</style>
