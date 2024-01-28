<template>
  <LockupGenerator/>
</template>

<script>
import LockupGenerator from './components/LockupGenerator.vue'

export default {
  name: 'App',
  components: {
    LockupGenerator
  }
}
</script>

<style>
#app {
  font-family: Amazon Ember, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
button {
  margin-left: 10px;
}
.club-name {
  font-size: 3em;
}
</style>
