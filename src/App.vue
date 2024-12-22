<template>
  <div class="container text-center mb-3">
    <img src="@/assets/amigo-invisible.png" alt="Girl in a jacket" style="width:75%; max-width:1000px">
  </div>
  <RulesViewer />
  <CheckMate />
</template>

<script>
import RulesViewer from './components/RulesViewer.vue'
import CheckMate from './components/CheckMate.vue'

export default {
  name: 'App',
  components: {
    RulesViewer,
    CheckMate
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
