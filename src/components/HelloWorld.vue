<template>
  <div class="hello">
    <knob />
  </div>
</template>

<script>
import knob from './v-knob.vue'
export default {
  components: {
    knob
  },
  name: 'slider',
  data () {
    return {
      max: '100',
      min: '0'
    }
  },
  mounted () {
    let target = document.querySelector('.rs-move')
    target.addClass = 'knob'
    console.log(target)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
