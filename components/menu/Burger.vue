<template>
  <div id="burger" :class="{ 'active' : isBurgerActive}" @click.prevent="toggle">
    <slot>
      <button type="button" class="burger-button" title="Menu">
        <span class="burger-bar burger-bar-1"></span>
        <span class="burger-bar burger-bar-2"></span>
        <span class="burger-bar burger-bar-3"></span>
      </button>
    </slot>
  </div>
</template>

<script>
import { store, mutations } from '@/store.js'
export default {
  computed: {
    isBurgerActive() {
      return store.isNavOpen
    }
  },

  methods: {
    toggle() {
      mutations.toggleNav()
    }
  }
}
</script>

<style lang="scss" scoped>
.hidden {
  visibility: hidden;
}

button {
  cursor: pointer;
}

button:focus {
  outline: none;
}

.burger-button {
  height: 30px;
  width: 32px;
  display: block;
  border: 0;
  border-radius: 0;
  background-color: transparent;
  pointer-events: all;
  transition: transform .6s cubic-bezier(.165,.84,.44,1);
  position: relative;
  margin: 20px;
  z-index: 999;
}

.burger-bar {
  background-color: $black;
  position: absolute;
  top: 50%;
  right: 6px;
  left: 6px;
  height: 2px;
  width: auto;
  margin-top: -1px;
  transition: transform .6s cubic-bezier(.165,.84,.44,1),opacity .3s cubic-bezier(.165,.84,.44,1),background-color .6s cubic-bezier(.165,.84,.44,1);
}

.burger-bar-1 {
  -webkit-transform: translateY(-6px);
  transform: translateY(-6px);
}

.burger-bar-2 {
  transform-origin: 100% 50%;
  transform: scaleX(.8);
}

.burger-button:hover .burger-bar-2 {
  transform: scaleX(1);
}

.no-touchevents .burger-bar-2:hover {
  transform: scaleX(1);
}

.burger-bar-3 {
  transform: translateY(6px);
}

#burger.active .burger-button {
  transform: rotate(-180deg);
}

#burger.active .burger-bar-1 {
  transform: rotate(45deg)
}

#burger.active .burger-bar-2 {
  opacity: 0;
}

#burger.active .burger-bar-3 {
  transform: rotate(-45deg)
}

@media only screen and (min-width: $desktop) {
  #burger {
    display: none;
  }
}
</style>