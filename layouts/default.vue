<template>
  <div>
    <Navbar />
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

body {
  background: $beige;
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

#pageWrap {
  margin: 0 auto;
  margin-bottom: 3rem;
}

</style>