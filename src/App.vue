<template>
  <div id="app">
    <Plan msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Plan from './views/Plan.vue'

export default {
  name: 'App',
  components: {
    Plan
  }
}
</script>

<style>
body, html {
  padding: 0;
  margin: 0;
}
</style>
