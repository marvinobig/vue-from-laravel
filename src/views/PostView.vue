<script setup lang="ts">
import ContentContainer from '@/components/ContentContainer.vue';

</script>

<template>
    <ContentContainer>
        <img class="aspect-16/9 object-cover rounded-lg my-3 mb-6" src="../assets/banner.jpg" alt="banner">

        <section class="flex items-center justify-between">
            <RouterLink class="bg-gray-800 py-2 px-5 rounded-lg text-white underline hover:text-blue-300"
                to="/posts/dummy-post">
                <h2 class="text-lg capitalize">Back</h2>
            </RouterLink>
            <p class="text-sm text-gray-500 capitalize">post date</p>
        </section>

        <section class="my-6">
            <h1 class="capitalize text-3xl font-bold">Individual post</h1>
        </section>

        <section class="bg-gray-800 text-white p-3 rounded-lg leading-9">
            <p>In the heart of the desert, where the sands shifted with the whims of the wind, Layla found a beauty
                unlike any other. The vast, empty expanse, with its dunes and mirages, held a silence that spoke
                volumes. The desert's harshness and its hidden oases were a metaphor for life's trials and unexpected
                blessings.</p>
            <br>
            <p>The annual fair, with its bright lights and lively music, was a celebration of community and tradition.
                Families gathered to enjoy the rides, games, and food, creating memories that would be cherished for
                years. For the townspeople, the fair was a reminder of the joy found in simple pleasures and the bonds
                that held them together.</p>
            <br>
            <p>In the heart of the rainforest, where the canopy formed a green cathedral, biologist Dr. Elena Sorensen
                conducted her research. The lush, vibrant ecosystem teemed with life, each species playing a role in the
                delicate balance of nature. Her work, a blend of science and passion, aimed to uncover the secrets of
                the forest and advocate for its preservation.</p>
            <br>
            <p>Beneath the starlit sky, where the constellations wove tales of gods and heroes, Layla found her
                inspiration. The night, with its velvet darkness and shimmering stars, was her muse. She would sit by
                the lake, sketchbook in hand, capturing the beauty of the cosmos in delicate lines and shades. Each
                drawing was a reflection of her dreams, a testament to her boundless imagination. The night sky, with
                its infinite mysteries, was a canvas for her creativity.</p>
            <br>
            <p>In the bustling newsroom, journalists raced against time to report the latest stories. The clatter of
                keyboards, the hum of conversations, and the flurry of activity created a palpable energy. For reporter
                Sarah, each day was a quest for truth, a commitment to informing the public and holding power to
                account.</p>
        </section>
    </ContentContainer>
</template>