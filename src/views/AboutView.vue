<script lang="ts">
  import CommonContent from '@/components/CommonContent.vue';
  import { Component, Vue } from 'vue-property-decorator';

  @Component({
    components: {
      CommonContent,
    },
  })
  export default class AboutView extends Vue {}
</script>

<template>
  <div class="about">
    <div>
      <h1>About</h1>
      <CommonContent text="詳細画面です" />
    </div>
  </div>
</template>

<style scoped>
  .about {
    display: flex;
    justify-content: center;
  }
</style>
