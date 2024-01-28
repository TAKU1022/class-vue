<script lang="ts">
  import { Component, Vue } from 'vue-property-decorator';
  import RootContent from './components/RootContent.vue';

  @Component({
    components: {
      RootContent,
    },
  })
  export default class App extends Vue {}
</script>

<template>
  <div id="app">
    <RootContent />
  </div>
</template>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    height: 100%;
  }
  html,
  body {
    margin: 0;
    padding: 0;
    height: 100%;
  }
</style>
