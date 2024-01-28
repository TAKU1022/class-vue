<script lang="ts">
  import { Component, Prop, Vue } from 'vue-property-decorator';

  @Component
  export default class CommonContent extends Vue {
    @Prop() public text!: string;
  }
</script>

<template>
  <div>
    <p>{{ text }}</p>
  </div>
</template>
