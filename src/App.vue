<template>
	<NavBar class="desktop-menu"></NavBar>
	<HamBurger class="mobile-menu"></HamBurger>
	<router-view/>
</template>
<script>
import NavBar from './components/NavBar.vue'
import HamBurger from './components/HamBurger.vue'
export default {
	name: 'App',
	components: {
		NavBar,
		HamBurger,
  }
}
</script>
<style lang="sass">
*
  margin: 0
  padding: 0
  box-sizing: border-box
@media (max-width: 460px)
	.desktop-menu
		display: none

@media (min-width: 461px)
	.mobile-menu
		display: none



</style>
