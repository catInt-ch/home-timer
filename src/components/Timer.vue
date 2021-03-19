<template>
  <div>
    <v-container class="mt-8">
      <v-row justify="center">
        <v-col
            v-for="time in times"
            :key="time.label" xs="4"
            class="text-h3 text-md-h2 ma-1 rounded-lg d-inline cat-int-light-background light-black-color">
          <div> {{ time.value }} </div>
          <div class="text-caption"> {{ time.label }} </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "Timer",
  data() {
    return {
      timeBetween: null
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
    },
    times: function () {
      return [
        { label: 'TAGE',      value: this.days },
        { label: 'STUNDEN',   value: this.hours },
        { label: 'MINUTEN',   value: this.minutes },
        { label: 'SEKUNDEN',  value: this.seconds }
      ]
    }
  },
  methods: {
    countdown() {
      this.timeBetween = new Date(2021, 3, 13, 8, 30) - new Date()
    }
  },
}
</script>

<style scoped>
.cat-int-light-color {
  color: #FFC6C6;
}

.cat-int-light-background {
  background-color: #FFC6C6;
}

.light-black-color {
  color: #1A1A18;
}
</style>
