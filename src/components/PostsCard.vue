<script setup>
const posts = [1, 2, 3, 4, 5, 6];
</script>

<template>
    <article class="flex flex-col gap-[3em]">
        <section class="flex flex-col sm:flex-row gap-3" v-for="(post, index) in posts" :key="index">
            <img src="../assets/post-img.jpg"
                class="aspect-square object-cover shadow-md rounded-lg w-full sm:max-w-[300px] sm:h-[300px]" alt="post">
            <div class="flex flex-col justify-between p-3 rounded-lg bg-gray-800 text-white w-full shadow-md">
                <div>
                    <RouterLink class="underline hover:text-blue-300" to="/posts/dummy-post">
                        <h2 class="font-bold text-2xl mb-4 capitalize">post title</h2>
                    </RouterLink>
                    <p>post summary</p>
                </div>
                <p class="text-sm text-blue-300 capitalize">post date</p>
            </div>
        </section>
    </article>
</template>