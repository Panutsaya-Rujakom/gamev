<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to your Vue.js App" /> -->
    <Game/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Counter from './components/Counter.vue'

export default {
    name: 'App',
    components: {
        //HelloWorld
        Game 
    }
}
</script>

<style>

</style>