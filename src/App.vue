<template>
  <div id="app">
    <List/>
  </div>
</template>

<script>
import List from './components/List'

export default {
  name: 'app',
  components: {
    List
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
