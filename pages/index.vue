<template>
  <section class="container">
      <div class="showcase toggle">
        <toggle />
      </div>

      <div class="showcase bag">
        <bag />
      </div>

      <div class="showcase heart">
        <heart />
      </div>

      <div class="showcase star">
        <star />
      </div>

  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Toggle from '~/components/Toggle.vue'
import Star from '~/components/Star.vue'
import Heart from '~/components/Heart.vue'
import Bag from '~/components/Bag.vue'

export default {
  components: {
    Logo,
    Toggle,
    Star,
    Heart,
    Bag
  }
}
</script>

<style lang="scss">
.container {
  display: flex;
  flex-direction: row;
  width: 100%;
  max-width: 100%;
  flex-wrap: wrap;

  @media only screen and (max-width: 820px) {

  }
}

.animation {
  cursor: pointer;
  max-width: 150px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}

.showcase {
    align-items: center;
    justify-content: center;
    display: flex;
    width: 49vw;
    flex-grow: 1;
    height: 50vh;
    
    @media only screen and (max-width: 820px) {
      height: 100vh;
      width: 100vw;
    }
}

.toggle {
  background: #06befb;
}
.star {
  background: #0293f4;
}
.heart {
  background: #E8EEF4;
}
.yepNope {
  background: #f1f9ff;
}
</style>
