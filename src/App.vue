<template>
  <NavBar></NavBar>
  
  <router-view/>
</template>
<script>
import NavBar from './components/NavBar.vue'
export default {
  name: 'App',
  components: {
    NavBar
  }
}
</script>
<style lang="sass">
*
  margin: 0
  padding: 0
  box-sizing: border-box
</style>
