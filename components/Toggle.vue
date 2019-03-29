<template>
  <div id="toggle" @click="play" class="animation">
  </div>
  
</template>

<script>
import lottie from 'lottie-web'

export default {
  data: () => ({
    anim: null,
    direction: 1,
  }),

  methods: {
    play(){
      this.anim.setDirection(this.direction)
      this.anim.setSpeed(1.5)
      this.anim.play()
      this.direction = this.direction * -1
    }
  },

  mounted(){
  this.anim = lottie.loadAnimation({
        container: this.$el, // the dom element that will contain the animation
        renderer: 'svg',
        loop: false,
        autoplay: false,
        animationData: require ('~/assets/toggle.json'), // the path to the animation json
        rendererSettings: {
          progressiveLoad: true, // Boolean, only svg renderer, loads dom elements when needed. Might speed up initialization for large number of elements.
        }
      });
  }
}  
</script>

<style>
.toggle {
}
</style>
