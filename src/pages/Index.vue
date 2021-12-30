<template>
  <div>
    <lottie-animation
      ref="anim"
      :animationData="require('src/assets/splash.json')"
      :loop="true"
      :autoPlay="true"
      :speed="1"
      @loopComplete="loopComplete"
      @complete="complete"
      @enterFrame="enterFrame"
    />
    <q-btn @click="stop">stop</q-btn>
    <q-btn @click="play">play</q-btn>
    <q-btn @click="pause">pause</q-btn>
    <q-btn @click="speedUp">speedUp</q-btn>
    <q-btn @click="speedDown">speedDown</q-btn>
  </div>
</template>

<script>
import LottieAnimation from 'lottie-web-vue'

export default {
  name: 'PageIndex',
  components: {
    LottieAnimation
  },
  mounted() {
    console.log(this.$refs.anim)
    this.$refs.anim.play()
  },
  methods: {
    loopComplete() {
      console.log('loopComplete')
    },
    complete() {
      console.log('complete')
    },
    enterFrame() {
      console.log('enterFrame')
    },
    stop() {
      this.$refs.anim.stop();
    },
    play() {
      this.$refs.anim.play();
    },
    pause() {
      this.$refs.anim.pause();
    },
    speedUp() {
      console.log(this.$refs.anim.speed)
      // this.$refs.anim.anim.setSpeed(1)
      console.log(this.$refs.anim.speed)
    },
    speedDown() {
      console.log(this.$refs.anim.speed)
      // this.$refs.anim.anim.setSpeed(1)
      console.log(this.$refs.anim.speed)
    },
  }
}
</script>
