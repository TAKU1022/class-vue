<script lang="ts">
  import CommonContent from '@/components/CommonContent.vue';
  import { Component, Vue } from 'vue-property-decorator';

  @Component({
    components: {
      CommonContent,
    },
  })
  export default class HomePage extends Vue {}
</script>

<template>
  <div class="home">
    <div>
      <h1>Home</h1>
      <CommonContent text="ホーム画面です" />
    </div>
  </div>
</template>

<style scoped>
  .home {
    display: flex;
    justify-content: center;
  }
</style>
