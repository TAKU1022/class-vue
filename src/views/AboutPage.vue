<script lang="ts">
  import CommonContent from '@/components/CommonContent.vue';
  import CounterButtons from '@/components/CounterButtons.vue';
  import { Component, Vue } from 'vue-property-decorator';

  @Component({
    components: {
      CommonContent,
      CounterButtons,
    },
  })
  export default class AboutPage extends Vue {
    counter = 0;

    addCounter() {
      this.counter += 1;
    }
    decrementCounter() {
      this.counter -= 1;
    }
  }
</script>

<template>
  <div class="about">
    <div>
      <h1>About</h1>
      <CommonContent text="詳細画面です" />
      <p>{{ counter }}</p>
      <CounterButtons
        @add-counter="addCounter"
        @decrement-counter="decrementCounter"
      />
    </div>
  </div>
</template>

<style scoped>
  .about {
    display: flex;
    justify-content: center;
  }
</style>
