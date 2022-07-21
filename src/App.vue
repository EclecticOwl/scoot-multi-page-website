<template>
  <!-- <NavBar></NavBar> -->
  <HamBurger></HamBurger>
  <router-view/>
</template>
<script>
// import NavBar from './components/NavBar.vue'
import HamBurger from './components/HamBurger.vue'
export default {
  name: 'App',
  components: {
    // NavBar,
    HamBurger
  }
}
</script>
<style lang="sass">
*
  margin: 0
  padding: 0
  box-sizing: border-box
</style>
