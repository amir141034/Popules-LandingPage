<script></script>
<template>
    <div class="flex flex-col fixed text-base-content bottom-0 bg-white text-base-content shadow-lg h-[calc(100vh-5rem)] w-64 p-4">
    <div class="flex flex-col gap-2">
      <div class="flex rounded-full font-semibold cursor-default select-none bg-gray-100 hover:bg-gray-100 p-3">
        <span class="mr-2" style="width: 1.5em; height: 1.5em; display: inline-block;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g fill="none"><path d="m12.593 23.258l-.011.002l-.071.035l-.02.004l-.014-.004l-.071-.035q-.016-.005-.024.005l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427q-.004-.016-.017-.018m.265-.113l-.013.002l-.185.093l-.01.01l-.003.011l.018.43l.005.012l.008.007l.201.093q.019.005.029-.008l.004-.014l-.034-.614q-.005-.018-.02-.022m-.715.002a.02.02 0 0 0-.027.006l-.006.014l-.034.614q.001.018.017.024l.015-.002l.201-.093l.01-.008l.004-.011l.017-.43l-.003-.012l-.01-.01z"></path><path fill="currentColor" d="M13.2 2.65a2 2 0 0 0-2.4 0l-7 5.25A2 2 0 0 0 3 9.5V19a2 2 0 0 0 2 2h3.9a1.1 1.1 0 0 0 1.1-1.1V15a2 2 0 1 1 4 0v4.9a1.1 1.1 0 0 0 1.1 1.1H19a2 2 0 0 0 2-2V9.5a2 2 0 0 0-.8-1.6z"></path></g></svg></span>
        Explore
      </div>

      <div class="flex rounded-full font-semibold cursor-default select-none hover:bg-gray-100 p-3">
        <span class="mr-2" style="width: 1.5em; height: 1.5em; display: inline-block;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill="currentColor" d="M11.5 4a3.5 3.5 0 1 0 0 7a3.5 3.5 0 0 0 0-7M6 7.5a5.5 5.5 0 1 1 11 0a5.5 5.5 0 0 1-11 0m12.872 6.994l-2.48 2.508h7.11v2h-7.11l2.48 2.508l-1.422 1.406l-4.858-4.914l4.858-4.914zM8 16a4 4 0 0 0-4 4h8.05v2H2v-2a6 6 0 0 1 6-6h4v2z"></path></svg></span>
        Following
      </div>

      <div class="flex rounded-full font-semibold cursor-default select-none hover:bg-gray-100 p-3">
        <span class="mr-2" style="width: 1.5em; height: 1.5em; display: inline-block;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g fill="none" fill-rule="evenodd"><path d="m12.594 23.258l-.012.002l-.071.035l-.02.004l-.014-.004l-.071-.036q-.016-.004-.024.006l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427q-.004-.016-.016-.018m.264-.113l-.014.002l-.184.093l-.01.01l-.003.011l.018.43l.005.012l.008.008l.201.092q.019.005.029-.008l.004-.014l-.034-.614q-.005-.019-.02-.022m-.715.002a.02.02 0 0 0-.027.006l-.006.014l-.034.614q.001.018.017.024l.015-.002l.201-.093l.01-.008l.003-.011l.018-.43l-.003-.012l-.01-.01z"></path><path fill="currentColor" d="M17.991 6.01L5.399 10.563l4.195 2.428l3.699-3.7a1 1 0 0 1 1.414 1.415l-3.7 3.7l2.43 4.194L17.99 6.01Zm.323-2.244c1.195-.433 2.353.725 1.92 1.92l-5.282 14.605c-.434 1.198-2.07 1.344-2.709.241l-3.217-5.558l-5.558-3.217c-1.103-.639-.957-2.275.241-2.709z"></path></g></svg></span>
        Messages
      </div>
      <div class="flex rounded-full font-semibold cursor-default select-none hover:bg-gray-100 p-3">
        <span class="mr-2" style="width: 1.5em; height: 1.5em; display: inline-block;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 256 256"><path fill="currentColor" d="M248 208h-16V96a8 8 0 0 0 0-16h-48V48a8 8 0 0 0 0-16H40a8 8 0 0 0 0 16v160H24a8 8 0 0 0 0 16h224a8 8 0 0 0 0-16M216 96v112h-32V96ZM56 48h112v160h-24v-48a8 8 0 0 0-8-8H88a8 8 0 0 0-8 8v48H56Zm72 160H96v-40h32ZM72 80a8 8 0 0 1 8-8h16a8 8 0 0 1 0 16H80a8 8 0 0 1-8-8m48 0a8 8 0 0 1 8-8h16a8 8 0 0 1 0 16h-16a8 8 0 0 1-8-8m-48 40a8 8 0 0 1 8-8h16a8 8 0 0 1 0 16H80a8 8 0 0 1-8-8m48 0a8 8 0 0 1 8-8h16a8 8 0 0 1 0 16h-16a8 8 0 0 1-8-8"></path></svg></span>
        Business
      </div>
      <div class="flex rounded-full font-semibold cursor-default select-none hover:bg-gray-100 p-3">
        <span class="mr-2" style="width: 1.5em; height: 1.5em; display: inline-block;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.618 21.25c0-3.602-4.016-6.53-7.618-6.53s-7.618 2.928-7.618 6.53M12 11.456a4.353 4.353 0 1 0 0-8.706a4.353 4.353 0 0 0 0 8.706"></path></svg></span>
        Profile
      </div>
      <div class="cursor-default border-t border-base-300 pt-4 py-2">
        <div class="text-gray-600 text-base mt-1 mb-3">Join our community now!</div>
        <div class="rounded-full font-semibold text-center cursor-pointer select-none border-2 bg-zinc-700 text-white hover:bg-white hover:text-gray-950 duration-200 p-3">
            Sign Up
        </div>
    </div>
    </div>
    

    <div class="border-t border-base-300 mt-auto pt-4">
        <div class="cursor-pointer rounded-lg text-center font-semibold w-full p-3">
        About
    </div>
      <div class="cursor-pointer rounded-lg text-center font-semibold w-full p-3">
        Privacy Policy
    </div>
    </div>
  </div>
</template>