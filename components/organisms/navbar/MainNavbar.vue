<template>
    <nav class="bg-white z-50 fixed top-0 left-0 w-full shadow-lg">
        <div
            class="container xl:max-w-screen-xl lg:max-w-screen-lg mx-auto flex justify-between items-center py-4 md:px-8 px-2">
            <!-- LogoText component on the left -->
            <!-- <router-link to="/">
        <AtomsLogoApp />
      </router-link> -->
            <h2 class="text-2xl font-bold font-onest">Kreati<span class="text-yellow-600">folk</span></h2>

            <ul class="flex flex-col md:flex-row space-y-4 md:space-y-0 md:space-x-8">
                <li v-for="(item, index) in menuItems" :key="index" class="relative group">
                    <router-link :to="item.to || ''" class="text-gray-800 font-medium hover:text-yellow-600 pb-2"
                        @click="isMobileMenuOpen = false">
                        {{ item.label }}
                    </router-link>
                    <span class="absolute bottom-0 left-0 w-0 h-[2px] bg-yellow-400 transition-all duration-300 group-hover:w-full"></span>
                </li>
            </ul>

        </div>
    </nav>
</template>

<script setup lang="ts">
import { ref } from 'vue';

interface IMenuItemProps {
    label: string;
    to: string;
}

interface IProps {
    logoText?: string;
    logoColor?: string;
    menuItems: IMenuItemProps[];
}

// Define props with default values
const props = withDefaults(defineProps<IProps>(), {
    logoColor: "text-gray-800", // Default logo color
});

// Control mobile menu visibility
const isMobileMenuOpen = ref(false);
</script>

<!-- <style scoped>
/* Custom styles for overlay effect on mobile */
@media (max-width: 767px) {
  .fixed {
    z-index: 40;
  }
  .bg-white {
    background-color: rgba(255, 255, 255, 0.95);
  }
}
</style> -->
