<template>
  <nav>
    <div class="main-menu">
        <div class="menu-links">
            <router-link to="/"><img :src="myLogo" alt="logo"></router-link>
            <router-link to="/about">About</router-link>
            <router-link to="/careers">Careers</router-link>
            <router-link to="/locations">Locations</router-link>
        </div>
        <div class="menu-cta">
            <button>Get Scootin</button>
        </div>
    </div>
    <div>
    </div>
  </nav>
</template>

<script>
import myLogo from '@/assets/logo.svg';
export default {
    name: 'NavBar',
    setup() {
        return {
            myLogo
        }
    },
}
</script>

<style lang="sass" scoped>
.main-menu
    display: flex
    justify-content: space-around
    padding: 1em 0
    img
        height: 25px
        width: auto
    a
        color: #B4B6BC
        text-decoration: none
    .menu-links
        display: flex
        align-items: center
        gap: 1.5em
    .menu-cta
        display: flex
        justify-content: center
        align-items: center
        button
            height: 100%
            padding: .75em 2em
            background-color: #F2BA4B
            border: none
            color: white
            border-radius: .25em
</style>