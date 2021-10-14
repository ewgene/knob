<template>
  <div id="app">
    <div class="wrapper">
      <knob @rotate="rotateKnob" />
    </div>
  </div>
</template>

<script>
import knob from './components/v-knob.vue'

export default {
  name: 'App',
  components: {
    knob
  },
  data () {
    return {
      targetInit: null,
      targetSupport: null
    }
  },
  methods: {
    rotateKnob () {
      this.targetInit = document.querySelector('.runner')
      this.targetSupport = document.querySelector('#app')
      console.log(this.targetSupport)
    }
  }
}
</script>

<style>
#app {
  width: 100%;
  height: 128px;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #090909;
  margin: 60px auto;
}
</style>
