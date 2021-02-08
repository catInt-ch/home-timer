<template>
  <v-app>
    <v-main class="light-black">
      <div id="app" class="pt-8 light-black">
        <img class="logo" alt="catInt logo" src="./assets/catInt_logo.png">
        <TimerContainer/>
      </div>
    </v-main>
  </v-app>
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
.light-black {
  background-color: #1A1A18;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #FF9398;
}

.logo {
  height: 10rem;
}
</style>
