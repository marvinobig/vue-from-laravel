<script setup>
import { useSearchStore } from '@/stores/search';

const searchStore = useSearchStore();
</script>

<template>
    <form class="flex justify-between gap-2 rounded-lg">
        <label class="capitalize" for="search" hidden>search</label>
        <input class="focus:outline-blue-300 bg-gray-800 text-white mb-6 p-4 rounded-lg text-lg w-full shadow-lg" type="search" id="search" placeholder="Search..."
            v-model="searchStore.search">
    </form>
</template>