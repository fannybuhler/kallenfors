<template>
  <div>
    <div class="landing-background"></div>
    <MenuNavbar />
    <div id="pageWrap">
      <Nuxt />
    </div>
    <Footer />
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
html {
  color: #000;
  font-family:
    Montserrat,
    sans-serif;
  font-size: 16px;
  line-height: 160%;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

body {
  background: $beige;
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

// * {
//   outline: 1px solid #f00 !important;
// }

.landing-background {
  height: 100vh;
  width: 100vw;
  max-width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  background-color: $white;
  z-index: -1;
}

#pageWrap {
  // margin-bottom: 3rem;
  // max-width: 1200px;
  // margin: 0 auto;
}

</style>
