<template>
  <div id="app">
    <el-switch
      v-model="mode"
      active-text="Part 2"
      inactive-text="Part1 and Part3"
      size="mini"
      style="margin-bottom:10vh;">
  </el-switch>
  <PeterNumber v-if="mode"/>
  <Calculator  v-else />
  </div>
</template>

<script>
import Calculator from './components/Calculator.vue'
import PeterNumber from './components/PeterNumber.vue'

export default {
  name: 'App',
  components: {
    Calculator,
    PeterNumber
  },
  data () {
    return {
      mode: false
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
