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
    const tl = gsap.timeline({ repeat: 2 , repeatDelay: 1})
    // timeline will go here
    tl.to('.first', { x: 700, duration: 2, ease: 'expo.out' })
    tl.to('.second', { x: 700, duration: 2, ease: 'expo.out' }, '<0.5')
    tl.to('.third', { x: 700, duration: 2, ease: 'expo.out' }, '<0.5')
  }
}
</script>

<style scoped>
.runner {
  display: block;
  height: 8em;
  width: 6em;
  margin-top: 1.5em;
}
</style>
