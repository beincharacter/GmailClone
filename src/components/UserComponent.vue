<template>
  <div id="UserComponent">
    <img
    @click="panel = !panel"
      data-tooltip-target="tooltip-no-arrow-user"
      data-tooltip-placement="bottom"
      src="https://placehold.co/80x80"
      alt="user"
      class="rounded-full cursor-pointer w-8"
    />
    <div
      id="tooltip-no-arrow-user"
      role="tooltip"
      class="inline-block absolute invisible text-xs z-10 py-1 px-2 font-medium text-black border rounded-sm shadow-sm tooltip dark:bg-gray-600 delay-150"
    >
      <div>Google Account</div>
      <div>Shubham Pal</div>
      <div class="text-gray-3">shubhampalatwork@gmail.com</div>
    </div>
    <div
    v-show="panel"
      class="absolute z-10 w-80 right-2 bg-white top-14 rounded-lg custom-shadow border"
    >
      <div class="w-full flex justify-center">
        <img
          class="rounded-full w-20 mt-4"
          src="https://placehold.co/80x80"
          alt="user"
        />
      </div><div class="text-gray-700 w-full flex justify-center mt-2 text-lg">
            Shubham Pal
        </div>
        <div class="text-gray-700 w-full flex justify-center text-sm pb-4 border-b">
            shubhampalatwork@gmail.com
        </div>
        <div class="flex justify-center my-5 p-4">
            <button class="bg-transparent text-xs hover:bg-gray-100 text-gray-600 font-semibold py-2 px-4 border border-gray-300 rounded">
                Sign out of Gmail
            </button>
        </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';


const panel = ref(false);
</script>
