<template>
  <div>
    <img class="runner first" src="../assets/toots.png" alt="runner" />
    <img class="runner second" src="../assets/toots.png" alt="runner" />
    <img class="runner third" src="../assets/toots.png" alt="runner" />
  </div>
</template>

<script>
import gsap from 'gsap'

export default {
  mounted() {
    // timeline will go here
  }
}
</script>

<style scoped>
.runner {
  display: block;
  height: 5em;
  width: 5em;
  margin-top: 1.5em;
}
</style>