
<template>
  <div id="app">
  <life-input v-model="motto"></life-input>
  <wonderfull-life v-for="n in 100" v-bind:message="motto"></wonderfull-life>
  </div>
</template>

<script>

import LifeInput from './LifeInput.vue'
import WonderfullLife from './WonderfullLife.vue'

export default {
  name: 'app',
  data () {
    return {
      motto: 'its a wonderfull life'
    }
  },
  components: {
    LifeInput,
    WonderfullLife
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
