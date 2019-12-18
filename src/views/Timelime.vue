<template>
    <div>
        <img class="runner first" src="../assets/toots.png" alt="runner"/>
        <img class="runner second" src="../assets/jerry.png" alt="runner"/>
        <img class="runner third" src="../assets/tom.png" alt="runner"/>
    </div>
</template>

<script>
import gsap from 'gsap'
    export default {
        mounted() {
            let tl = gsap.timeline();
            tl.to('.first', { x: 900, y:100, duration: 2, ease: 'expo.out'})
            tl.to('.second', { x: 800, y: -50, duration: 2, ease: 'expo.out'})
            tl.to('.third', { x: 700,y: -150, duration: 2, ease: 'expo.out'})
        }

        
    }
</script>

<style scoped>
.runner {
    display: block;
    height: 9em;
    width: 8em;
    margin-left: -200px;
    margin-top: 1.5em;
}

</style>