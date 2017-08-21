<template>
  <div id="app">
    <nav class="topnav"><h3 class="logo">GeTaLaB</h3></nav>
    <home></home>
  </div>
</template>

<script>
import Home from './components/Home'

export default {
  name: 'app',
  components: {
    Home
  }
}
</script>

<style>
nav.topnav {
  position: fixed;
  top: 0;
  width: 100vw;
  z-index: 100;
  background-color: rgba(255,255,255,0.0);
  color: white;
}
</style>
