<script lang="ts">
  import { Component, Prop, Vue } from 'vue-property-decorator';

  @Component
  export default class PostCard extends Vue {
    @Prop() public postId!: number;
  }
</script>

<template>
  <div>
    <div>{{ postId }}</div>
  </div>
</template>
