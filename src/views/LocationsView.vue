<template>
  <header>
		<h1>
			Locations
		</h1>
	</header>
    <main>
        <img class="img-desktop" src="@/assets/images/world-map-desktop.png" alt="world map">
        <img class="img-mobile" src="@/assets/images/world-map-mobile.png" alt="world map">
        <div class="map1"><p class="jakarta">Jakarta</p></div>
        <div class="map2"><p class="london">London</p></div>
        <div class="map3"><p class="new_york">New York</p></div>
        <div class="map4"><p class="yokohama">Yokohama</p></div>
    </main>
    <section>
        <div class="locations-container">
            <h1>New York</h1>
            <h1>London</h1>
            <h1>Jakarta</h1>
            <h1>Yokohama</h1>
        </div>
        <h1>Your city not listed?</h1>
        <p>If you'd like to see Scoot in your hometown, be sure to let us know. We track 
  requests and plan launches based on demand. Feel free to message us by clicking 
  the link or messaging us on social.</p>
        <a href="#">Message Us</a>
    </section>

</template>

<script>
export default {
    name: 'LocationsView',
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

main
    margin-top: 2em
    display: flex
    flex-direction: column
    justify-content: center
    align-items: center
    position: relative

    img
        height: auto
        width: 800px
    
    .jakarta, .london, .new_york, .yokohama
        position: relative
        background: #F1BA4B
        padding: .5em 1em
        color: white

    .jakarta::after, .london::after, .new_york::after, .yokohama::after
        content: ''
        position: absolute
        bottom: 0
        left: 50%
        width: 0
        height: 0
        border: 20px solid transparent
        border-top-color: #F1BA4B
        border-bottom: 0
        margin-left: -20px
        margin-bottom: -20px
    .map1
        position: absolute
        transform: translate(230px, 8px)
    .map2
        top: 20px
        transform: translateX(-45px)
        position: absolute
    .map3
        position: absolute
        top: 65px
        transform: translateX(-225px)
    .map4
        position: absolute
        transform: translate(290px, -115px)
.locations-container
    margin-top: 4em
    display: flex
    flex-direction: column
    justify-content: center
    align-items: center
    gap: 1em
    h1
        background-color: #FCF4E0
        padding: .5em 1em
        width: 200px
        text-align: center
section
    margin-top: 3em
    padding: 0 10em
    display: flex
    justify-content: center
    align-items: center
    gap: 2em
    p   
        font-size: .7em
        width: 400px
    a
        text-decoration: none
        background-color: #F2BA4B
        color: white
        padding: .5em 1em
@media (max-width: 800px)
    header
        display: flex
        justify-content: center
        padding: 4em 0
    main
        img
            width: 100%
    .map1, .map2, .map3, .map4, .img-desktop
        display: none
    section
        flex-direction: column

        p
            width: 300px

@media (min-width: 800px)
    .img-mobile, .locations-container
        display: none



</style>