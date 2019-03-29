<template>
  <div id="heart" @click="play" class="animation">
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
      this.anim.setSpeed(2)
      this.anim.play()
      this.anim.goToAndPlay(1)
    }
  },

  mounted(){
  this.anim = lottie.loadAnimation({
        container: this.$el, // the dom element that will contain the animation
        renderer: 'svg',
        loop: false,
        autoplay: false,
        animationData: require ('~/assets/heart.json'), // the path to the animation json
        rendererSettings: {
          progressiveLoad: true,
        }
      });
  }
}  
</script>

<style>
.heart {
  
}
</style>
