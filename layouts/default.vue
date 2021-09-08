<template>
  <div>
    <MenuNavbar />
    <div class="landing-background"></div>
    <div id="pageWrap">
      <Nuxt />
    </div>
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

h3 {
  line-height: 160%;
  font-size: 24px;
  font-weight: 300;
}

p {
  font-size: 16px;
  line-height: 160%;
}

body {
  background: $beige;
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

.landing-background {
  height: 100vh;
  width: 100vw;
  position: absolute;
  top: 0;
  left: 0;
  background-color: $white;
  z-index: -1;
}

#pageWrap {
  margin-bottom: 3rem;
  max-width: 1200px;
  margin: 0 auto;

  @media only screen and (max-width: $desktop) {
    max-width: 950px;
  }


  @media only screen and (max-width: $tablet) {
    max-width: 720px;
  }
}

</style>