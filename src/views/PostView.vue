<script setup lang="ts">
import { ref, onMounted } from 'vue';
import { useRoute } from 'vue-router';
import ContentContainer from '@/components/ContentContainer.vue';
import moment from 'moment';

const post = ref(null);
const route = useRoute();

onMounted(async () => {
  try {
    const id = route.params.id;
    const url = `http://127.0.0.1:8000/api/v1/posts/${id}`;
    const request = await fetch(url);

    if (!request.ok) {
      throw new Error(`Request for post: ${id} failed`);
    }

    const response = await request.json();

    post.value = response.post;

  } catch (err) {
    console.error(`${err.message}`);
  }
});
</script>

<template>
  <ContentContainer>
    <img class="aspect-16/9 object-cover rounded-lg my-3 mb-6" src="../assets/banner.jpg" alt="banner">

    <section v-if="post" class="flex items-center justify-between">
      <RouterLink class="bg-gray-800 py-2 px-5 rounded-lg text-white hover:text-blue-300" to="/posts">
        <h2 class="text-lg capitalize">Back</h2>
      </RouterLink>
      <p class="text-sm text-gray-500 capitalize">{{ moment(post.created_at).format('dddd LL') }}</p>
    </section>

    <section v-if="post" class="my-6">
      <h1 class="capitalize text-3xl font-bold">{{ post.title }}</h1>
    </section>

    <section v-if="post" class="bg-gray-800 text-white p-3 rounded-lg leading-9">
      <p>
        {{ post.body }}
      </p>
    </section>

    <section v-else class="capitalize bg-gray-800 text-white p-3 rounded-lg leading-9">
      <p>
        post does not exist
      </p>
    </section>
  </ContentContainer>
</template>
