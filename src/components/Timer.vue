<template>
  <div>
    <h2 class="text-h2 mt-8 cat-int-light">{{ days }} : {{ hours }} : {{ minutes }} : {{ seconds }}</h2>
  </div>
</template>

<script>
export default {
  name: "Timer",
  data() {
    return {
      timeBetween: null,
    }
  },
  mounted() {
    setInterval(this.countdown, 1000);
  },
  computed: {
    days: function () {
      const days = Math.floor((this.timeBetween) / (1000 * 60 * 60 * 24)).toString()
      return "0".concat(days).slice(-2)
    },
    hours: function () {
      const hours = (Math.floor((this.timeBetween) / (1000 * 60 * 60)) % 24).toString()
      return "0".concat(hours).slice(-2)
    },
    minutes: function () {
      const minutes = (Math.floor((this.timeBetween) / (1000 * 60)) % 60).toString()
      return "0".concat(minutes).slice(-2)
    },
    seconds: function () {
      const seconds = (Math.floor((this.timeBetween) / 1000) % 60).toString()
      return "0".concat(seconds).slice(-2)
    }
  },
  methods: {
    countdown() {
      this.timeBetween = new Date(2021, 1, 26, 9, 0) - new Date()
    }
  },
}
</script>

<style scoped>
.cat-int-light {
  color: #FFC6C6;
}
</style>
