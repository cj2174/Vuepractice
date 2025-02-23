<template>
  <div>
    <Post :posts="posts[i]" v-for="(a, i) in posts" :key="i" />
  </div>
</template>

<script>
import Post from "./Post.vue";
export default {
  components: {
    Post,
  },
  props: {
    posts: Array,
  },
};
</script>

<style></style>
