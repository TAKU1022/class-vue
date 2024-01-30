<script lang="ts">
  import { Component, Vue } from 'vue-property-decorator';

  @Component
  export default class CounterButtons extends Vue {
    addCount() {
      this.$emit('add-count');
    }
    decrementCount() {
      this.$emit('decrement-count');
    }
  }
</script>

<template>
  <div class="buttons">
    <button @click="addCount">add</button>
    <button @click="decrementCount">decrement</button>
  </div>
</template>

<style scoped>
  .buttons {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 4px;
  }
</style>
