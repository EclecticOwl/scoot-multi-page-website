<template>
	<div class="home">
		<div class="hero-container">
			<div class="hero-text">
				<h1>Scooter sharing made simple</h1>
				<p>Scoot takes the hassle out of urban mobility. Our bikes are placed in convenient 
  locations in each of our cities. Use our app to locate the nearest bike, unlock 
  it with a tap, and you're away!
  </p>
				<a class="btn-cta">Get Scootin</a>
			</div>
			<div class="hero-bubbles">
				<img :src="whiteCircles" alt="white circles used to decorate page">
			</div>
		</div>
		
	</div>
</template>


<script>
import whiteCircles from '@/assets/patterns/white-circles.svg'
export default {
	name: 'HomeView',
	components: {
	},
	setup() {
		return {
			whiteCircles
		}
	}
}
</script>

<style lang="sass" scoped>
@import url('https://fonts.googleapis.com/css2?family=Space+Mono&display=swap')
.home
	color: white
	font-family: 'Space Mono', monospace
.hero-container
	position: relative
	background-image: url('@/assets/images/home-hero-desktop.jpg')
	background-size: contain no-repeat
	background-position: center
	height: 500px
	overflow: hidden
.hero-text
	position: relative
	padding-left: 10em
	display: flex
	flex-direction: column
	justify-content: center
	gap: 3em
	height: 100%
	h1
		width: 250px
		font-size: 1.4em

	p
		position: relative
		margin-left: 2em
		width: 300px
	p::before
		top: 40%
		position: absolute
		content: ''
		background-image: url("@/assets/patterns/line.svg?inline")
		height: 12px
		width: 200px
		transform: translateX(-230px)
	p::after
		position: absolute
		top: 40%
		right: 1
		content: ''
		background-image: url('@/assets/patterns/right-arrow.svg?inline')
		background-size: cover 
		height: 130px
		width: 400px
		transform: translateX(200px)
	.btn-cta
		padding: .5em 1em
		margin-left: 2em
		width: 150px
		background-color: #F2BA4B
		text-align: center
		border-radius: .25em
.hero-bubbles
	position: absolute
	bottom: 120px
	right: 0
	transform: translateX(50px)
@media (max-width: 1150px)
	.hero-text
		align-items: center
		justify-content: flex-start
		padding-left: 0
		p::before, p::after
			display: none
		h1
			margin-top: 1em
			text-align: center
	
	.hero-text::before
		position: absolute
		bottom: 5%
		left: 0
		content: ' '
		background-image: url('@/assets/patterns/right-arrow.svg?inline')
		background-size: cover
		height: 100px
		width: 300px
		
	.hero-bubbles
		bottom: 20px
@media (max-width: 500px)
	.hero-text::before
		bottom: 5%
		height: 110px
		width: 330px
		background-size: contain no-repeat
		background-position: bottom 100px
		transform: translateX(-205px)
	.hero-bubbles
		display: none



</style>