<template>
  <nav class="navbar">
    <!-- Not the best solution using mediaqueries in each component to determine mobile or desktop navigation-->
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
          <NuxtLink to="/kontakt">Kontakt</NuxtLink>
        </li>
      </ul>
    </MenuSidebar>
    <MenuDesktop />
  </nav>
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
  font-size: 18px;
  display: flex;
  justify-content: flex-end;
  padding: 20px;
  background: $white;

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
  .navbar {
    justify-content: center;
  }
}
</style>
