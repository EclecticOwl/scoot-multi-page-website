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
		<div class="three-column">
			<div class="three-column-item">
				<img src="@/assets/icons/locate.svg?inline" alt="locate icon">
				<div class="three-column-info">
					<h2>Locate with app</h2>
					<p>
					Use the app to find the nearest scooter to you. We are continuously placing scooters 
	in the areas with most demand, so one should never be too far away. 
					</p>
				</div>
			</div>
			<div class="three-column-item">
				<img src="@/assets/icons/scooter.svg?inline" alt="scooter icon">
				<div class="three-column-info">
					<h2>Pick your scooter</h2>
					<p>
						We show the most important info for the scooters closest to you. So you know how much 
	charge they have left and can see roughly how much it will cost.
					</p>
				</div>
			</div>
			<div class="three-column-item">
				<img src="@/assets/icons/ride.svg?inline" alt="ride icon">
				<div class="three-column-info">
					<h2>Enjoy the ride</h2>
					<p>
						Scan the QR code and the bike will unlock. Retract the cable lock, put on a helmet, 
	and you're off! Always lock bikes away from walkways and accessibility ramps.
					</p>
				</div>
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
	font-family: 'Space Mono', monospace
.hero-container
	color: white
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
.three-column
	margin-top: 7em
	display: flex
	padding-left: 7em
	gap: 3em
	position: relative

	img
		height: 75px
		width: auto
	h2
		font-size: 1.2em
		color: #495567
	p
		font-size: .5em
		color:  #939CAA
.three-column::before
		position: absolute
		bottom: 70%
		left: 0
		content: ' '
		background-image: url('@/assets/patterns/line.svg?inline')
		background-size: cover
		filter: grayscale(100%)
		z-index: -1
		height: 10px
		width: 875px
.three-column-item
		width: 325px


@media (max-width: 1100px)
	.three-column
		flex-direction: column
		justify-content: center
		align-items: center
		max-width: 100%
	.three-column::before
		display: none
	.three-column::after
		position: absolute
		content: ' '
		top: 0
		left: 10px
		background-image: url('@/assets/patterns/line.svg?inline')
		background-size: cover
		filter: grayscale(100%)
		z-index: -1
		height: 10px
		width: 800px
		transform: rotate(90deg) translateY(16.5em)
		
	.three-column-item
		display: flex
		width: 100%
		gap:  6em
		p
			margin-top: 3em
			width: 200px
		
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
	.three-column::after
		display: none
	.three-column
		padding-left: 0
	.three-column-item
		gap: 1em
		flex-direction: column
		align-items: center
		justify-content: center
		img
			width: 75px
	.three-column-info
		text-align: center
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