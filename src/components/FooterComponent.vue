<template>
<footer>
	<div class="footer-top">
		<h1>
			Sign up and Scoot off today
		</h1>
		<div>
			<img src="@/assets/icons/app-store.svg?inline" alt="app store icon">
			<img src="@/assets/icons/google-play.svg?inline" alt="google play icon">
		</div>
	</div>
	<div class="footer-bottom">
		<div class="footer-links">
            <router-link to="/"><img class="logo" :src="myLogo" alt="logo"></router-link>
            <router-link to="/about">About</router-link>
            <router-link to="/careers">Careers</router-link>
            <router-link to="/locations">Locations</router-link>
        </div>
		<div class="footer-icons">
			<img src="@/assets/icons/facebook.svg?inline" alt="facebook icon">
			<img src="@/assets/icons/twitter.svg?inline" alt="twitter icon">
			<img src="@/assets/icons/instagram.svg?inline" alt="instagram icon">
		</div>
	</div>
</footer>
</template>

<script>
import myLogo from '@/assets/logo.svg';
export default {
	name: 'FooterComponent',
	setup() {
		return {
			myLogo
		}
	},
}
</script>

<style lang="sass" scoped>
footer
	margin-top: 5em
	display: grid
	grid-template-rows: 2fr 1fr
	gap: 2em
	background-color: #4B5465

.footer-top, .footer-bottom
	width: 100%
.footer-top, .footer-bottom
	padding: 1em 7em
	display: flex
	justify-content: space-between
	align-items: center
	div
		display: flex
		justify-content: center
		align-items: center
		gap: 1em
img
	height: 40px
.logo
	filter: brightness(0) invert(1)
.footer-top
	color: white
	position: relative
	h1, div
		z-index: 2
.footer-top::after
	bottom: 0
	right: 40px
	position: absolute
	content: ''
	background-image: url("@/assets/patterns/white-circles.svg?inline")
	background-size: cover
	height: 80px
	width: 700px
	transform: translateY(32px)
	filter: invert(50%) grayscale(100%)
	
.footer-bottom
	background-color: #343943
	img
		height: 20px
a
	color: #949BA9
	text-decoration: none

@media(max-width: 700px)
	.footer-top
		flex-direction: column
		gap: 1em
		text-align: center
	.footer-bottom
		padding: 1em 2em

@media (max-width: 500px)
	.footer-top
		justify-content: center
		gap: 3em
	.footer-bottom, .footer-links
		display: flex
		flex-direction: column
	.footer-bottom
		gap: 3em



</style>