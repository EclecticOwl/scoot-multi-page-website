<template>
	<NavBar class="desktop-menu"></NavBar>
	<HamBurger class="mobile-menu"></HamBurger>
	<router-view/>
	<FooterComponent></FooterComponent>
</template>
<script>
import NavBar from './components/NavBar.vue'
import HamBurger from './components/HamBurger.vue'
import FooterComponent from './components/FooterComponent.vue'
export default {
	name: 'App',
	components: {
		NavBar,
		HamBurger,
		FooterComponent,
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
