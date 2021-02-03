<template>
  <div id="app">
    <img class="logo" alt="catInt logo" src="./assets/catInt_logo.png">
    <TimerContainer/>
  </div>
</template>

<script>
import TimerContainer from './components/TimerContainer.vue'

export default {
  name: 'App',
  components: {
    TimerContainer
  }
}
</script>

<style>
body {
  background-color: #000000;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #FF9398;
  margin-top: 60px;
}

.logo {
  height: 10rem;
}
</style>
