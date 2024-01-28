<script lang="ts">
  import { Component, Vue } from 'vue-property-decorator';
  import MainHeader from './MainHeader.vue';
  import MainFooter from './MainFooter.vue';

  @Component({
    components: {
      MainHeader,
      MainFooter,
    },
  })
  export default class RootContent extends Vue {}
</script>

<template>
  <div class="root">
    <MainHeader />
    <nav class="nav">
      <router-link to="/">Home</router-link>
      <span>|</span>
      <router-link to="/about">About</router-link>
    </nav>
    <main class="main">
      <router-view />
    </main>
    <MainFooter />
  </div>
</template>

<style scoped>
  .root {
    display: flex;
    flex-direction: column;
    height: 100%;
  }
  .nav {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 8px;
  }
  .main {
    flex: 1;
    min-height: 0;
    padding-top: 40px;
  }
</style>
