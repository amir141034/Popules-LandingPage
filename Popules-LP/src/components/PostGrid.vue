<script setup>
import PostCard from './PostCard.vue'

defineProps({
  posts: {
    type: Array,
    default: () => []
  }
})
</script>

<template>
    <div class="columns-1 sm:columns-3 lg:columns-5 gap-4">
    <PostCard
      v-for="(post, index) in posts"
      :key="index"
      :post="post"
    />
  </div>
</template>