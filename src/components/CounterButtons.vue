<script lang="ts">
  import { Component, Vue } from 'vue-property-decorator';

  @Component
  export default class CounterButtons extends Vue {
    addCounter() {
      this.$emit('add-counter');
    }
    decrementCounter() {
      this.$emit('decrement-counter');
    }
  }
</script>

<template>
  <div class="buttons">
    <button @click="addCounter">add</button>
    <button @click="decrementCounter">decrement</button>
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
