<template>
  <div>
    <Header/>
    <CardSection/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import CardSection from './components/CardSection.vue';
export default {
  name: 'App',
  components: {
    Header,
    CardSection
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
