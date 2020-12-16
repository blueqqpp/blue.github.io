<template>
  <div id="app">
    <home></home>
  </div>
</template>

<script>
import Home from './components/home/Home'
export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
}
#app {
  background-color: #fafafa;
}
</style>
