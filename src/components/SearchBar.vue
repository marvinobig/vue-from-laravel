<script setup>
// import { useSearchStore } from '@/stores/search';

// const searchStore = useSearchStore();
</script>

<template>
    <form class="flex justify-between gap-2 bg-gray-800 p-3 rounded-lg">
        <label class="capitalize" for="search" hidden>search</label>
        <input class="focus:outline-blue-300 bg-white px-4 py-2 rounded-lg text-lg w-full" type="search" id="search"
            v-model="searchStore.search">
    </form>
</template>