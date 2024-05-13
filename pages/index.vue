<template>
    <main>
      <header-imagen :source="'/foto1.jpg'" />
      <section>
      <h1>{{title}}</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Aut, quaerat architecto. Necessitatibus, assumenda quis esse est maxime pariatur? Tempora at harum aut vitae magni quam exercitationem in molestiae eius quisquam.
      </p>
      </section>
      <section class="container cards-section">
        <article-card
        v-for="(article, index) in articles"
        :key="index"
        :article="article"
        />
      </section>
    </main>
</template>

<script setup>
import {ref} from 'vue'
const title = ref('Página de inicio')

const articles = ref([
  {
    id: 1,
    title: "Articulo 1",
    foto: "https://picsum.photos/500/300"
  },
  {
    id: 2,
    title: "Articulo 2",
    foto: "https://picsum.photos/500/301"
  },
  {
    id: 3,
    title: "Articulo 3",
    foto: "https://picsum.photos/500/302"
  },
  {
    id: 4,
    title: "Articulo 4",
    foto: "https://picsum.photos/500/303"
  },
])
</script>

<style lang="postcss"> 
  .cards-section{
    display: flex;
    justify-content: space-between;
  }
</style>