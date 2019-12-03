<template>
  <div>
    <div :style="{ width: tweenedNumber + 'px' }" class="bar">
      <span>{{ number }}</span>
    </div>
  </div>
</template>

<script>
import gsap from 'gsap'
export default {
  data() {
    return {
      number: 0,
      tweenedNumber: 0
    }
  },

  watch: {
    number(newValue) {
      gsap.to(this.$data, {
        duration: 0.5,
        ease: 'circ.out',
        tweenedNumber: newValue
      })
    }
  },
  methods: {
    randomNumber() {
      this.number = Math.floor(Math.random() * (800 - 0))
    }
  },

  created() {
    setInterval(this.randomNumber, 1500)
  }
}
</script>

<style scoped>
.bar {
  padding: 20px;
  border: rgb(105, 48, 48) solid;
  background-color: salmon;
}
</style>
