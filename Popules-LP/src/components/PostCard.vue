<script setup>
import {ref} from 'vue'

defineProps({
  post: {
    type: Object,
    required: true
  }
})

const isModalOpen = ref(false)

</script>

<template>
    <div  @click="isModalOpen = true" class="break-inside-avoid  shadow hover:shadow-xl transition-shadow bg-white mb-4">
    <div class="p-3">
        <img
        :src="post.thumbnail"
        alt="Post image"
        loading="lazy"
        class="w-full hover:brightness-75 object-cover"
        />
      <h2 class="font-semibold text-sm my-2">{{ post.title }}</h2>
      <div class="flex justify-between">
        <div class="flex items-center">
            <img
            :src="post.user.logo_url"
            alt="Post image"
            loading="lazy"
            class="w-4 h-4 rounded-full  object-cover"
            />
            <p class="text-gray-500 text-xs ml-1">{{ post.user.fullname }}</p>
        </div>
        <span class="w-4 h-4 rounded-full  stroke-gray-500 text-transparent hover:text-red-500 transition-all duration-200 transform hover:scale-150">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
            <path d="M16.696 3C14.652 3 12.887 4.197 12 5.943C11.113 4.197 9.348 3 7.304 3C4.374 3 2 5.457 2 8.481s1.817 5.796 4.165 8.073S12 21 12 21s3.374-2.133 5.835-4.446C20.46 14.088 22 11.514 22 8.481S19.626 3 16.696 3z"/>
        </svg>
        </span>

      </div>
    </div>
  </div>
  <Teleport to="#modal">
      <div class="modal-bg h-screen w-screen" v-if="isModalOpen"> 
        <div class="modal">
          <button @click="isModalOpen = false" class="close-btn text-lg">X</button>
            <img
            :src="post.thumbnail"
            alt="Post image"
            loading="lazy"
            class="modalImg rounded-lg object-cover"
            />
            <div class="relative p-6 w-96 border-l border-base-300 h-full">
              <div class="flex items-center justify-between">
                <div class="flex items-center">
                    <img
                    :src="post.user.logo_url"
                    alt="Post image"
                    loading="lazy"
                    class="w-4 h-4 rounded-full object-cover"
                    />
                    <p class="text-gray-900 font-semibold text-sm ml-1">{{ post.user.fullname }}</p>
                </div>
                <div class="postBtn cursor-pointer font-semibold hover:bg-pink-500">Follow</div>
              </div>
              <div class="mt-6 font-semibold text-sm">{{ post.title }}</div>
              <div class="mt-1 text-sm">{{ post.content }}</div>
              <div class="my-4 text-xs text-gray-500">{{ new Date(post.published_at).toLocaleDateString('en-US', { month: 'short', day: 'numeric' }) }}</div>
              <div class="pt-4 text-gray-500 border-t border-base-300">No comments</div>
              <div class="flex items-center justify-between absolute p-4 h-16 w-full left-0 bottom-0 border-t border-base-300">
                <form class="search pr-6">
                    <input 
                    type="text"
                    name="searchQuery"
                    placeholder="Add Comments"/>
                </form>
                  <span class="w-4 h-4 rounded-full  scale-150 stroke-gray-900 text-transparent hover:text-red-500 transition-all duration-200 transform">
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
                      <path d="M16.696 3C14.652 3 12.887 4.197 12 5.943C11.113 4.197 9.348 3 7.304 3C4.374 3 2 5.457 2 8.481s1.817 5.796 4.165 8.073S12 21 12 21s3.374-2.133 5.835-4.446C20.46 14.088 22 11.514 22 8.481S19.626 3 16.696 3z"/>
                  </svg>
                  </span>
              </div>
            </div>
        </div>
      </div>
    </Teleport>
</template>
