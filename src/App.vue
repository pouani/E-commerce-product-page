<template>
  <div class="px-4 md:px-32">
    <nav-bar />
    <Home />
  </div>
</template>

<script>
import Home from './components/Home.vue'
import NavBar from './components/NavBar.vue'
export default {
  name: 'App',
  components: {
    Home,
    NavBar
  }
}
</script>
