<template>
  <div>
    <BodyView/>
  </div>
</template>

<script>
import BodyView from './components/BodyView.vue';
export default {
  name: 'App',
  components: {
    BodyView
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
