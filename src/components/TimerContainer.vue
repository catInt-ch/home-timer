<template>
  <div class="timer">
    <h1 class="text-h2 text-md-h1 mt-2 mt-md-6">Kitten Timer</h1>
    <Timer/>
  </div>
</template>

<script>
import Timer from "@/components/Timer";
export default {
  name: 'TimerContainer',
  components: { Timer },
  props: { }
}
</script>

<style scoped>
.timer-title{
  font-size: 10rem;
  margin: 0;
}
</style>
