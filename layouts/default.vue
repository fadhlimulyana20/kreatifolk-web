<script setup lang="ts">
const menuItems = ref([
    {
        label: "Tentang Kami",
        to: "/about",
    },
    {
        label: "Showcase",
        to: "/showcase",
    },
]);
</script>

<template>
    <div>
        <OrganismsNavbarMainNavbar :menu-items="menuItems" />
        <div class="">
            <slot></slot>
        </div>
    </div>
</template>
