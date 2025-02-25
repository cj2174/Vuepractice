<template>
  <div>
    <div v-if="step == 0">
      <Post :posts="posts[i]" v-for="(a, i) in posts" :key="i" />
    </div>

    <!-- 필터선택페이지 -->
    <div v-if="step == 1">
      <div class="upload-image"></div>
      <div class="filters">
        <div class="filter-1"></div>
        <div class="filter-1"></div>
        <div class="filter-1"></div>
        <div class="filter-1"></div>
        <div class="filter-1"></div>
      </div>
    </div>

    <!-- 글작성페이지 -->
    <div v-if="step == 2">
      <div class="upload-image"></div>
      <div class="write">
        <textarea class="write-box">write!</textarea>
      </div>
    </div>
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
    step: Number,
  },
};
</script>

<style></style>
