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
		<main>
			<div class="main-col-1">
				<div class="main-col-img">
					<img src="@/assets/images/telemetry.jpg" alt="picture of person holding phone">
				</div>
				<div class="main-col-info">
					<h1>Easy to use riding telemetry</h1>
					<p>The Scoot app is available with riding telemetry. This means it can show you your 
  average speed, how long you've been using the scooter, your traveling distance, 
  and many more things all in an easy to use app.</p>
					<a class="main-col-cta" href="">Learn more</a>
				</div>
			</div>
			<div class="main-col-2">
				<div class="main-col-img">
					<img src="@/assets/images/near-you.jpg" alt="picture of city">
				</div>
				<div class="main-col-info">
					<h1>Coming to a city near you</h1>
					<p>Scoot is available in 4 major cities so far. We're expanding rapidly, so be sure 
  to let us know if you want to see us in your hometown. We're aiming to let our 
  scooters loose on 23 cities over the coming year.</p>
					<a class="main-col-cta" href="">Learn more</a>
				</div>
			</div>
			<div class="main-col-3">
				<div class="main-col-img">
					<img src="@/assets/images/payments.jpg" alt="picture of person holding wallet">
				</div>
				<div class="main-col-info">
					<h1>Zero hassle payments</h1>
					<p>Our payment is as easy as one two three. We accept most credit cards and debit cards. 
  You can also link your PayPal account inside the app. Need to pay later? No worries! 
  You can defer payment for up to a month.</p>
					<a class="main-col-cta" href="">Learn more</a>
				</div>
			</div>
		</main>
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
	font-size: .8em
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
		color: #495567
	p
		
		color:  #939CAA
.three-column::before
		position: absolute
		bottom: 80%
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
main
	margin-top: 7em
.main-col-1, .main-col-2, .main-col-3
	margin-top: 6em
	display: flex
	flex-direction: row-reverse
	justify-content: space-around
	gap: 10em
	position: relative
	p
		color: #939CAA
	p, h1
		width: 500px
		margin-bottom: 2em
	img
		height: 300px
		border-radius: 10em
	a
		text-decoration: none
		background-color: #F2BA4B
		padding: .5em 2em
		color: white
.main-col-2
	flex-direction: row

.main-col-1::after, .main-col-3::after
	position: absolute
	top: 0
	right: 0
	content: ' '
	background-image: url('@/assets/patterns/circle.svg?inline')
	background-size: contain
	height: 300px
	width: 300px
	transform: translateX(220px)
.main-col-2:after
	position: absolute
	top: 0
	left: 0
	content: ' '
	background-image: url('@/assets/patterns/circle.svg?inline')
	background-size: contain
	height: 300px
	width: 300px
	transform: translateX(-220px)
.main-col-1::before
	position: absolute
	top: 0
	right: 0
	content: ' '
	background-image: url('@/assets/patterns/left-downward-arrow.svg?inline')
	background-size: cover
	background-size: no-repeat
	z-index: 1
	height: 140px
	width: 550px
	transform: translate(120px, 200px)
.main-col-2::before
	position: absolute
	top: 0
	left: 0
	content: ' '
	background-image: url('@/assets/patterns/right-arrow.svg?inline')
	background-size: cover
	background-size: no-repeat
	z-index: 1
	height: 130px
	width: 400px
	transform: translateX(-140px)
.main-col-3::before
	position: absolute
	top: 0
	right: 0
	content: ' '
	background-image: url('@/assets/patterns/left-downward-arrow.svg?inline')
	background-size: cover
	background-size: no-repeat
	z-index: 1
	height: 140px
	width: 550px
	transform: translate(300px, 50px)
@media (max-width: 1100px)
	.main-col-1, .main-col-2, .main-col-3
		flex-direction: column
		align-items: center
		justify-content: center
		gap: 5em
		h1, p
			margin-top: 1em
	.main-col-info
		padding: 0 2em
		display: flex
		flex-direction: column
		justify-content: center
		align-items: center
		a
			width: 150px
			text-align: center
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
		left: 0
		background-image: url('@/assets/patterns/line.svg?inline')
		background-size: cover
		filter: grayscale(100%)
		z-index: -1
		height: 10px
		width: 1000px
		transform: rotate(90deg) translateY(29em)
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
	
	.main-col-1::before, .main-col-3::before
		transform: translate(300px, 200px)
	.main-col-1::after, .main-col-2::after, .main-col-3::after
		display: none
	.main-col-info
		text-align: center
		p, h1
			width: 300px
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