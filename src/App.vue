<template>
  <div id="app">
    <div class="knob">
      <slider />
    </div>
  </div>
</template>

<script>
import slider from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    slider
  },
  data () {
    return {
      range: {
        high: null,
        low: null
      }
    }
  }
}
</script>

<style>
#app {
  width: 128px;
  height: 128px;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #090909;
  margin: 60px auto;
}
.knob {
  width: 128px;
  height: 128px;
  background-image: url('./assets/knob-bg.png');
}
</style>
