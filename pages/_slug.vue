<template>
  <div>
    <h1 class="text-2xl">{{ post.title }}</h1>
    <div v-html="post.html"/>
  </div>
</template>

<script>
  import { getSinglePost } from '../api/posts';

  export default {
    async asyncData ({ params }) {
      const post = await getSinglePost(params.slug);
      return { post: post }
    }
  }
</script>