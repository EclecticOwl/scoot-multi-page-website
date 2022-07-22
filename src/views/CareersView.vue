<template>
  <header>
		<h1>
			Careers
		</h1>
	</header>
    <main>
		<div class="main-col-1">
			<div class="main-col-img">
				<img src="@/assets/images/join-us.jpg" alt="picture of person holding tablet in meeting">
			</div>
			<div class="main-col-info">
				<h1>Care to join our mission?</h1>
				<p>We're always looking for ambitious individuals to help us on our journey. If you’re 
  passionate about our mission to provide clean, accessible transport to improve urban 
  living we want to hear from you!</p>
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
		<div class="job-container">
			<div class="job-item">
				<div class="job-title">
					<span>General Manager</span>
					<p>Jakarta, Indonesia</p>
				</div>
				<div class="job-cta"><a href="#">Apply</a></div>
			</div>
			<div class="job-item">
				<div class="job-title">
					<span>UI/UX Designer</span>
					<p>Yokohama, Japan</p>
				</div>
				<div class="job-cta"><a href="#">Apply</a></div>
			</div>
			<div class="job-item">
				<div class="job-title">
					<span>Blog Content Copywriter</span>
					<p>New York, United States</p>
				</div>
				<div class="job-cta"><a href="#">Apply</a></div>
			</div>
			<div class="job-item">
				<div class="job-title">
					<span>Fleet Supervisor</span>
					<p>Jakarta, Indonesia</p>
				</div>
				<div class="job-cta"><a href="#">Apply</a></div>
			</div>
			<div class="job-item">
				<div class="job-title">
					<span>Graphic Designer</span>
					<p>New York, United States</p>
				</div>
				<div class="job-cta"><a href="#">Apply</a></div>
			</div>
			<div class="job-item">
				<div class="job-title">
					<span>UX Analyst</span>
					<p>London, United Kingdom</p>
				</div>
				<div class="job-cta"><a href="#">Apply</a></div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
    name: 'CareersView',
}
</script>

<style lang="sass" scoped>
*
	font-family: 'Space Mono', monospace
p
	font-size: .9em
	color: #949BA9

// Header Section

header
	background-image: url('@/assets/images/careers-locations-hero-desktop.jpg')
	height: 200px
	display: flex
	align-items: center
	padding-left: 5em
	color: white
	font-size: 1.5em

// Main Section

main
	overflow: hidden
.main-col-1
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
.main-col-info
	width: 300px
	display: flex
	flex-direction: column
	gap: 2em
	text-align: center
.main-col-1::before
	position: absolute
	top: 0
	right: 0
	content: ' '
	background-image: url('@/assets/patterns/left-downward-arrow.svg?inline')
	background-size: cover
	background-size: no-repeat
	z-index: 1
	height: 150px
	width: 550px
	transform: translate(90px, 160px)
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

// Section Piece
section
	margin-top: 10em
	display: flex
	flex-direction: column
	align-items: center
	gap: 6em
	padding: 0 14em
	h1
		font-size: 1.7em
.value-container
	display: flex
	align-items: center
	justify-content: center
	gap: 7em
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
.job-container
	display: flex
	flex-direction: column
	gap: 1em
	width: 100%
.job-item
	padding: .25em 2em
	background-color: #F2F4F9
	display: flex
	justify-content: space-between
	align-items: center
.job-cta a
	text-decoration: none
	background-color: #F1BA4B
	color: white
	padding: .5em 2em
	font-size: .7em
@media (max-width: 800px)
	.main-col-1
		flex-direction: column
		align-items: center
	section
		padding: 0 8em
	.value-container
		flex-direction: column
@media (max-width: 500px)
	header
		display: flex
		justify-content: center
		padding: 4em 0
	section
		padding: 0 1em
	.main-col-1::after, .main-col-1::before
		display: none


</style>