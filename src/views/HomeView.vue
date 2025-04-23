<script setup>
import ContentContainer from '@/components/ContentContainer.vue';

</script>

<template>
  <main>
    <ContentContainer>
      <h1 class="my-8 text-3xl font-bold text-center text-gray-800">The Vue From WordPress</h1>

      <section class="leading-9 text-center my-8 text-gray-800">
        <h2 class="text-xl font-semibold mb-2">Rational</h2>
        <p>
          The best way to learn is by building real, hands-on projects. I'm using Vue and laravel
          to create a custom blog frontend from scratch. This project helps me understand how modern tools
          work together in a practical setup. It’s a unique, portfolio-worthy build that reflects real-world
          development workflows.
        </p>
      </section>

      <section class="leading-9 text-center my-8 text-gray-800">
        <h2 class="text-xl font-semibold mb-2">Aim</h2>
        <p>
          Build a site using a laravel backend with a Vue frontend to display content.
          The goal is to gain practical experience with Vue and laravel in a real-world workflow.
        </p>
      </section>

      <section class="leading-9 text-center my-8 text-gray-800">
        <h2 class="text-xl font-semibold mb-2">Functional Requirements</h2>
        <ul class="list-inside">
          <li>Posts can be added through laravel backend</li>
          <li>Users can view posts through a separate interface</li>
        </ul>
      </section>

      <section class="leading-9 text-center my-8 text-gray-800">
        <h4 class="text-md font-semibold mb-2">Developed by marvinobig</h4>
      </section>
    </ContentContainer>
  </main>
</template>
