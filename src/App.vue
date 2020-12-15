<template>
  <div id="app">
    <face/>
  </div>
</template>

<script>
  import face from './components/organisms/face.vue'
  export default {
    name: 'App',
    components: {
      face
    }
  }
</script>

<style lang="scss">
  @font-face {
    font-family: "Pacifico";
    src: url("assets/fonts/Pacifico.ttf");
  }

  @font-face {
    font-family: "Axis";
    src: url("assets/fonts/axis.woff") format("woff");
  }

  @font-face {
    font-family: "Montserrat";
    src: url("assets/fonts/Montserrat-Bold.ttf") format("woff");
  }

  body {
    margin: 0;
    overflow-x: hidden;
  }

  .body--disable-scroll {
    height: 100%;
    overflow: hidden;
  }

  img {
    -webkit-user-drag: none;
    -webkit-user-select: none;
  }

  a {
    text-decoration: none;
  }
</style>
