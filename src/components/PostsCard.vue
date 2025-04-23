<script setup>
import { ref, onMounted, watch } from 'vue';
import { useSearchStore } from '@/stores/search';
import moment from 'moment';

const posts = ref([]);
const filteredPosts = ref([]);
const query = useSearchStore();

onMounted(async () => {
  try {
    const request = await fetch('http://127.0.0.1:8000/api/v1/posts');

    if (!request.ok) {
      throw new Error("Request Failed");
    }

    const response = await request.json();
    posts.value = response.posts.filter((post) => post.status).reverse();
    filteredPosts.value = posts.value;
  } catch (err) {
    console.error(`${err.message}`);
  }
});

watch(() => query.search, (newSearch) => {
  const search = newSearch.toLowerCase();

  filteredPosts.value = posts.value.filter((post) =>
    post.title.toLowerCase().includes(search)
  );
});
</script>

<template>
  <article class="flex flex-col gap-[1em]">
    <section class="flex flex-col sm:flex-row gap-3" v-for="(post, index) in filteredPosts" :key="index">
      <div class="flex items-center justify-between p-3 rounded-lg bg-gray-800 text-white w-full shadow-md">
        <div class="flex flex-col gap-2">
          <h2 class="font-bold text-2xl capitalize">{{ post.title }}</h2>
          <p class="text-sm text-blue-300 capitalize">{{ moment(post.created_at).format('dddd LL') }}</p>
        </div>
        <RouterLink class="capitalize rounded-lg bg-blue-300 py-2 px-4 text-black cursor-pointer"
          :to="`/posts/${post.id}`">
          view
        </RouterLink>
      </div>
    </section>

    <section v-if="!posts">
      <p>No Posts Available</p>
    </section>
  </article>
</template>
