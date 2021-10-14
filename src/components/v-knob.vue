<template>
  <div class="knob" :style="knobBack" @mousedown="rotateKnob">
    <div class="runner">
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
      active: false,
    }
  },
  methods: {
    rotateKnob () {
      this.$emit('rotate')
    }
  },
  computed: {
    knobBack() {
      return {
        backgroundImage: require('../assets/knob-bg.png')
      }
    }
  }
}
</script>

<style lang="css" scoped>
  .knob {
    width: 128px;
    height: 128px;
    margin: 0 auto;
    background-image: url('../assets/knob-bg.png');
  }
  .runner {
    width: 128px;
    height: 128px;
    background-image: url('../assets/knob-full.png');    
  }
</style>
