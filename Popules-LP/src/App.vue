<script setup>
import Navbar from '@/components/Navbar.vue'
import Sidebar from '@/components/Sidebar.vue'
import PostGrid from '@/components/PostGrid.vue'

import { ref, onMounted, onBeforeUnmount } from 'vue'
import axios from 'axios'

const posts = ref([])
const offset = ref(0)
const limit = 25
const loading = ref(false)
const loadMoreTrigger = ref(null)
let observer

const fetchPosts = async () => {
  if (loading.value) 
  return loading.value = true
  try {
    const res = await axios.get('https://api.popules.com/api/feed', {
      params: { offset: offset.value, limit }
    })
    const newPosts = res.data.data
    if (newPosts.length > 0) {
      posts.value.push(...newPosts)
      offset.value += limit
    } else {
      observer && observer.disconnect()
    }
  } catch (err) {
    console.error(err)
  } finally {
    loading.value = false
  }
}

onMounted(() => {
  fetchPosts()

  observer = new IntersectionObserver((entries) => {
    if (entries[0].isIntersecting) {
      fetchPosts()
    }
  })
  observer.observe(loadMoreTrigger.value)
})

onBeforeUnmount(() => observer && observer.disconnect())

const wordTag=['All', 'Vacancies', 'Workplace', 'Food', 'Design', 'Cars', 'Finance', 'Lifestyle', 'Travel', 'Makeup', 'Fitness']

</script>

<template>
    <div class="home overflow-y-auto scrollbar-hide h-screen">
      <Sidebar/>
      <!-- Main Content -->
      <div class="bg-gray-50 ml-64 mt-24 h-screen">
        <ul class="flex m-3">
            <li v-for="tag in wordTag" class="tag select-none hover:bg-gray-200 p-3 mx-1">
                {{ tag }}
            </li>
        </ul>
          <div class="h-full px-4">
            <PostGrid :posts="posts" />
            <div v-if="loading" class="text-center text-gray-500 py-4">
              Loading more...
            </div>
            <div ref="loadMoreTrigger" class="h-10"></div>
          </div>
        </div>
    </div>
    <Navbar />
</template>