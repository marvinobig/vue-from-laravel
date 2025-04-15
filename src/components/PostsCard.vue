<script setup>
const posts = [1, 2, 3, 4, 5, 6];
</script>

<template>
    <article class="flex flex-col gap-[3em]">
        <section class="flex gap-3" v-for="(post, index) in posts" :key="index">
            <img src="" class="rounded-lg border border-blue-800 w-full max-w-[250px] h-[250px]" alt="post">
            <div class="p-3 rounded-lg bg-gray-800 text-white capitalize w-full">
                <a class="underline hover:text-blue-300" href="post-link">
                    <h2 class="font-bold text-2xl mb-3">post title</h2>
                </a>
                <p>post summary</p>
                <p>post date</p>
            </div>
        </section>
    </article>
</template>