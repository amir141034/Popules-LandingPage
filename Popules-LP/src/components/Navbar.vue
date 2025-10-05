<script setup>
import logo from '@/assets/popules_logo.png'
</script>

<template>
<nav class="fixed bg-white border-b top-0 w-full px-6">
      <div class="flex items-center justify-between h-20">
        <div class="flex flex-1 items-center justify-center">
            <div class="flex items-center mx-4">
                <img class="h-12 w-auto" :src="logo" alt="Popules" />
            </div>
            <form class="search mx-8">
                <input 
                type="text"
                name="searchQuery"
                placeholder="Search..."/>
                <span class="absolute flex items-center pr-3"><span class="text-gray-400" style="width: 1.7em; height: 1.7em; display: inline-block;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><path d="m21 21l-4.34-4.34"></path><circle cx="11" cy="11" r="8"></circle></g></svg></span></span>
            </form>
          <div class="ml-auto">
            <div class="flex items-center justify-center">
                <div class="postBtn font-semibold hover:bg-pink-500 mx-1">Post</div>
                <div class="iconCircle bg-gray-300 mx-1"><span style="width: 1.2em; height: 1.2em; display: inline-block;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill="currentColor" d="M14.235 19c.865 0 1.322 1.024.745 1.668A4 4 0 0 1 12 22a4 4 0 0 1-2.98-1.332c-.552-.616-.158-1.579.634-1.661l.11-.006zM12 2c1.358 0 2.506.903 2.875 2.141l.046.171l.008.043a8.01 8.01 0 0 1 4.024 6.069l.028.287L19 11v2.931l.021.136a3 3 0 0 0 1.143 1.847l.167.117l.162.099c.86.487.56 1.766-.377 1.864L20 18H4c-1.028 0-1.387-1.364-.493-1.87a3 3 0 0 0 1.472-2.063L5 13.924l.001-2.97A8 8 0 0 1 8.822 4.5l.248-.146l.01-.043a3 3 0 0 1 2.562-2.29l.182-.017z"></path></svg></span></div>
                <div class="iconCircle bg-gray-300 mx-1"><span style="width: 1.7em; height: 1.7em; display: inline-block;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><path d="M18 20a6 6 0 0 0-12 0"></path><circle cx="12" cy="10" r="4"></circle><circle cx="12" cy="12" r="10"></circle></g></svg></span></div>

            </div>
          </div>
        </div>
      </div>
  </nav>
</template>