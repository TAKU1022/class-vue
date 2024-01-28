<script lang="ts">
  import PostCard from '@/components/PostCard.vue';
  import { Component, Vue } from 'vue-property-decorator';

  @Component({
    components: {
      PostCard,
    },
  })
  export default class PostPage extends Vue {
    postId = parseInt(this.$route.params.postId);
  }
</script>

<template>
  <div class="post">
    <div>
      <h1>Post</h1>
      <PostCard :postId="postId" />
    </div>
  </div>
</template>

<style scoped>
  .post {
    display: flex;
    justify-content: center;
  }
</style>
