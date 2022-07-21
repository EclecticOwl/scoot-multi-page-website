<template>
  <nav>
    <div>
        <img :src="myLogo" alt="logo">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
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

<style lang="sass">

</style>