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
	<section>
		<h1>Our Values</h1>
		<div class="value-container">
			<div class="value-item">
			<div class="value-image">
				<img src="@/assets/images/our-tech.jpg" alt="person holding phone">
				<p>01</p>
			</div>
			<div class="value-info">
				<h3>Our Tech</h3>
				<p>
					We're using cutting edge technology to drive accessible urban transportation forward. 
  Our fully electric scooters are a joy to ride!
				</p>
			</div>
		</div>
		<div class="value-item">
			<div class="value-image">
				<img src="@/assets/images/our-integrity.jpg" alt="a person riding a scooter">
				<p>02</p>
			</div>
			<div class="value-info">
				<h3>Our integrity</h3>
				<p>
					We are fully committed to deliver a great yet safe, sustainable micro-mobility experience 
  in every city we serve.
				</p>
			</div>
		</div>
		<div class="value-item">
			<div class="value-image">
				<img src="@/assets/images/our-community.jpg" alt="picture of people crossing crosswalk">
				<p>02</p>
			</div>
			<div class="value-info">
				<h3>Our community</h3>
				<p>
					We support every community we serve. All workers are paid a living wage based on their 
  location and are Scoot employees.
				</p>
			</div>
		</div>
		</div>
	</section>
	<section>
		<h1>FAQs</h1>

		<div class="faq-container">
			<h2>How it works</h2>
			<div class="faq-1">

				<div class="faq-item">
				<div class="faq-title" @click="show1 = !show1">
					<span>How do I download the app?</span>
					<img v-if="show1" src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
					<img class="invert" v-else src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
			
				</div>
				<Transition name="fade">
					<p v-if="show1">To download the Scoot app, you can search “Scoot” in both the App and Google Play stores. 
	An even simpler way to do it would be to click the relevant link at the bottom of this 
	page and you'll be re-directed to the correct page.</p>
				</Transition>
				</div>

				<div class="faq-item">
				<div class="faq-title" @click="show = !show">
					<span>Can I find nearby Scoots?</span>
					<img v-if="show" src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
					<img class="invert" v-else src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
			
				</div>
				<Transition name="fade">
					<p v-if="show">Definitely! Simply open up the app and allow us to find your location while using it. We'll 
  show you all of the closest Scoots and some extra useful information.</p>
				</Transition>
				</div>

				<div class="faq-item">
				<div class="faq-title" @click="show2 = !show2">
					<span>Do I need a license to ride?</span>
					<img v-if="show2" src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
					<img class="invert" v-else src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
			
				</div>
				<Transition name="fade">
					<p v-if="show2">Yup! We provide information inside the app regarding local laws and the license you need to be 
  able to ride our Scoots.</p>
				</Transition>
				</div>
			</div>
		</div>

		<div class="faq-container">
			<h2>Safe driving</h2>
			<div class="faq-1">

				<div class="faq-item">
				<div class="faq-title" @click="show3 = !show3">
					<span>Should I wear a helmet?</span>
					<img v-if="show3" src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
					<img class="invert" v-else src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
			
				</div>
				<Transition name="fade">
					<p v-if="show3">Yes, please do! All cities have different laws. But we strongly strongly strongly recommend 
  always wearing a helmet regardless of the local laws. We like you and we want you to be as 
  safe as possible while Scooting.</p>
				</Transition>
				</div>

				<div class="faq-item">
				<div class="faq-title" @click="show4 = !show4">
					<span>How about the rules & regulations?</span>
					<img v-if="show4" src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
					<img class="invert" v-else src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
			
				</div>
				<Transition name="fade">
					<p v-if="show4">Now is not the time to be a rule breaker. Be sure you're complying with all local laws and 
  regulations. Also, just be a good human being. Be sure not to park your Scoot where it can 
  block access to buildings or get in people's way.</p>
				</Transition>
				</div>

				<div class="faq-item">
				<div class="faq-title" @click="show5 = !show5">
					<span>What if I damage my Scoot?</span>
					<img v-if="show5" src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
					<img class="invert" v-else src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
			
				</div>
				<Transition name="fade">
					<p v-if="show5">Be sure to read our terms and conditions carefully. Not the most fun job we know but we make 
  it as clear as possible. There's an option to add insurance for each trip, or you can sign 
  up for annual insurance if you're a regular Scooter.</p>
				</Transition>
				</div>
			</div>
		</div>

	</section>
</template>

<script>
export default {
	name: 'AboutView',
	data()  {
		return {
			show: false,
			show1: false,
			show2: false,
			show3: false,
			show4: false,
			show5: false,
		}
	}
}
</script>

<style lang="sass" scoped>
@import url('https://fonts.googleapis.com/css2?family=Space+Mono&display=swap')
*
	font-family: 'Space Mono', monospace
p
	font-size: .9em
	color: #949BA9
header
	background-image: url('@/assets/images/about-hero-desktop.jpg')
	height: 200px
	width: auto
	display: flex
	align-items: center
	padding-left: 5em
	color: white
	font-size: 1.5em
	overflow: hidden
main
	overflow: hidden
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
section
	margin-top: 10em
	display: flex
	flex-direction: column
	align-items: center
	gap: 6em
	padding: 0 2em
	overflow: hidden
	h1
		font-size: 1.7em
.value-container
	display: flex
	align-items: center
	justify-content: center
	gap: 5em
	img
		height: auto
		width: 150px
		border-radius: 6em
.value-item
	display: flex
	flex-direction: column
	justify-content: center
	align-items: center
	width: 250px
.value-image
	display: flex
	flex-direction: column
	align-items: center
	p
		margin-top: -1em
		background-color: #F2BA4B
		padding: .5em
		border-radius: 1em
		color: white
.value-info
	margin-top: 1em
	gap: 1em
	display: flex
	flex-direction: column
	align-items: center
	p
		text-align: center
.fade-enter-active, .fade-leave-active 
  transition: opacity .5s ease
.fade-enter-from, .fade-leave-to 
  opacity: 0
.faq-item
	margin-top: .5em
	display: flex
	flex-direction: column
	justify-content: center
	align-items: center
	gap: 1em
	width: 500px
	background-color: #F2F4F9
	padding: .75em 3em
.faq-title
	width: 100%
	display: flex
	flex-direction: row
	justify-content: space-between
	align-items: center
	img
		height: 15px
		width: 15px
.faq-container
	width: 100%
	display: flex
	justify-content: space-between
	padding: 0 10em
.invert
	transform: rotate(180deg)

@media (max-width: 800px)
	.faq-container
		flex-direction: column
		justify-content: center
		align-items: center
		gap: 1em
	.main-col-1, .main-col-2
		flex-direction: column
		align-items: center
	.value-container
		flex-direction: column

@media (max-width: 500px)
	header
		display: flex
		justify-content: center
		padding: 4em 0
	.faq-item
		width: 350px
	.main-col-1::after, .main-col-2::after
		display: none
	.main-col-1::before
		transform: translate(250px, 200px)
	
</style>