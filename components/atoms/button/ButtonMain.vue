<template>
  <button class="rounded-lg bg-gray-400 pb-[5px] shadow-md">
    <div
      class="w-full px-4 py-2 bg-gray-200 hover:bg-gray-300 rounded-lg font-bold text-lg border-t-2 border-gray-50 hover:border-gray-100 text-gray-700"
    >
      <slot></slot>
    </div>
  </button>
</template>

<script setup lang="ts">
import { ref } from "vue";

// interface IProps {
//     logoText?: string;
//     logoColor?: string;
// }

// // Define props with default values
// const props = withDefaults(defineProps<IProps>(), {
//     logoColor: "text-gray-800", // Default logo color
// });

// Control mobile menu visibility
const isMobileMenuOpen = ref(false);
</script>
