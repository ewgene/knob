<template>
  <div class="hello">
    <knob
      radius="63"
      width="8"
      showTooltip="false"
      pathColor="#090909"
      rangeColor="transparent" />
  </div>
</template>

<script>
import knob from 'vue-round-slider'
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
  mounted: function () {
    let target = document.querySelector('.rs-move')
    target.addClass = 'knob'
    console.log(target)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
