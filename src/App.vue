<template>
  <div id="app">
    <face/>
    <home/>
    <about/>
    <building/>
    <gallery/>
    <tail/>
  </div>
</template>

<script>
import face from './components/organisms/face.vue'
import home from './components/organisms/home.vue'
import about from './components/organisms/about.vue'
import building from './components/organisms/building.vue'
import gallery from './components/organisms/gallery.vue'
import tail from './components/organisms/tail.vue'

export default {
  name: 'App',
  components: {
    face,
    home,
    about,
    building,
    gallery,
    tail
  },
  data() {
    
  }
}
</script>

<style>

</style>
