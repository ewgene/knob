<template>
  <div class="knob" :style="{ 'background-image': 'url(./knob-full.png)'}" @mousedown="rotateKnob">
    <div class="runner" :style="{ 'background-image': 'url(./knob-full.png)'}">
    </div>
  </div>
</template>

<script>
export default {
  name: 'v-knob',
  props: {
    min: {
      type: [String, Number],
      default: 0
    },
    max: {
      type: [String, Number],
      default: 100
    },
    step: {
      type: [String, Number],
      default: 1
    },
    back: {
      type: [String],
      default: '../assets/knob-bg.png'
    },
    knob: {
      type: [String],
      default: '../assets/knob-full.png'
    },
    start: {
      type: [String, Number],
      default: '-45deg'
    }
  },
  data () {
    return {
      targetInit: null,
      targetSupport: null,
      active: false
    }
  },
  methods: {
    rotateKnob () {
      this.$emit('rotate')
    }
  }
}
</script>

<style lang="css" scoped>
  .knob {
    width: 128px;
    height: 128px;
    margin: 0 auto;
  }
  .runner {
    width: 128px;
    height: 128px;
  }
</style>
