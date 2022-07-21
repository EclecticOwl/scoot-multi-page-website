<template>
  <nav>
        <div class="hamburger-box" :class="{ isActive: isActive}">
            <button class="hamburger" :class="{ isActive: isActive }" @click="isActive = !isActive">
                <div class="bar"></div>
            </button>
		</div>
        <div class="menu" :class="{ showMenu: isActive}">
            <div class="menu-links">
                <router-link to="/">Home</router-link>
                <router-link to="/about">About</router-link>
                <router-link to="/careers">Careers</router-link>
                <router-link to="/locations">Locations</router-link>
            </div>
        </div>
  </nav>
</template>

<script>
export default {
    name: 'HamBurger',
    data() {
		return {
			isActive: true
		}
	},
}
</script>

<style lang="sass" scoped>
.hamburger-box
	position: fixed
	z-index: 100
	top: 1rem
	left: 1rem
	padding: 4px
	border: #F2BA4B solid 2px
	background: white
	cursor: pointer
	width:  45px
	transition: 0.2s
.hamburger 
	display: block
	width: 35px
	cursor: pointer
	appearance: none
	background: none
	outline: none
	border: none
.hamburger .bar, .hamburger:after, .hamburger:before 
	content: ''
	display: block
	width: 100%
	height: 3px
	background-color: black
	margin: 6px 0px
	transition: transform 0.4s
.hamburger.isActive:before
	background-color: #F2BA4B
	transform: rotate(-45deg) translate(-7px, 5px)
.hamburger.isActive:after
	background-color: #F2BA4B
	transform: rotate(45deg) translate(-7px, -7px)
.hamburger.isActive .bar 
	opacity: 0
.hamburger-box.isActive
	background-color: black
	border: white solid 2px
.menu
	position: fixed
	transform: translateY(-100%)
	transition: transform 0.4s
	top: 0
	left: 0
	right: 0
	bottom: 0
	z-index: 99
	background: white
	color: white
	padding-top: 4rem
.menu-links
    display: flex
    flex-direction: column
    justify-content: center
    align-items: center
    height: 100%
    gap: 3em
    a
        background-color: #F2BA4B
        padding: 1em 2em
        width: 150px
        text-align: center
        border-radius: 2em
        text-decoration: none
        color: white
    a:hover
        background-color: white
        color: #F2BA4B
        border: 1px solid black

.showMenu 
	transform: translateY(0)
</style>