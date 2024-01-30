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
    count = 0;

    addCount() {
      this.count += 1;
    }
    decrementCount() {
      this.count -= 1;
    }
  }
</script>

<template>
  <div class="about">
    <div>
      <h1>About</h1>
      <CommonContent text="詳細画面です" />
      <p>{{ count }}</p>
      <CounterButtons @add-count="addCount" @decrement-count="decrementCount" />
    </div>
  </div>
</template>

<style scoped>
  .about {
    display: flex;
    justify-content: center;
  }
</style>
