<template>
	<header>
		<h1>
			About
		</h1>
	</header>
	<main>
		<div class="main-col-1">
			<div class="main-col-img">
				<img src="@/assets/images/digital-era.jpg" alt="picture of person holding phone">
			</div>
			<div class="main-col-info">
				<h1>Mobility for the digital era</h1>
				<p>Getting around should be simple (and even fun!) for everyone. We embrace technology to 
  provide low cost, smart access to scooters at your fingertips.</p>
			</div>
		</div>
		<div class="main-col-2">
			<div class="main-col-img">
				<img src="@/assets/images/better-living.jpg" alt="picture of person holding phone">
			</div>
			<div class="main-col-info">
				<h1>Better urban living</h1>
				<p>We're helping connect cities and bring people closer together. Our scooters are also 
  fully-electric and we offset the minimal carbon footprint for each ride.</p>
			</div>
		</div>
	</main>
</template>

<script>
export default {
	name: 'AboutView',
}
</script>

<style lang="sass" scoped>
@import url('https://fonts.googleapis.com/css2?family=Space+Mono&display=swap')
*
	font-family: 'Space Mono', monospace
header
	background-image: url('@/assets/images/about-hero-desktop.jpg')
	height: 200px
	display: flex
	align-items: center
	padding-left: 5em
	color: white
	font-size: 1.5em
.main-col-1, .main-col-2
	margin-top: 6em
	display: flex
	flex-direction: row-reverse
	justify-content: space-around
	gap: 10em
	position: relative
	img
		height: auto
		width:  300px
		border-radius: 10em
.main-col-2
	flex-direction: row
.main-col-info
	width: 300px
	display: flex
	flex-direction: column
	gap: 2em
	text-align: center
.main-col-1::after
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

@media (max-width: 800px)
	.main-col-1, .main-col-2
		flex-direction: column
		align-items: center


@media (max-width: 500px)
	.main-col-1::after, .main-col-2::after
		display: none
	.main-col-1::before
		transform: translate(250px, 200px)
	
</style>