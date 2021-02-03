<template>
  <div class="timer">
    <h1 class="timer-title">Home Timer</h1>
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
