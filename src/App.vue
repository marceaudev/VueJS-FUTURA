<script setup>
import ArticleCard from './components/ArticleCard.vue'
import Footer from './components/Footer.vue'
import FrontPage from './components/FrontPage.vue'
import Header from './components/Header.vue'
import data from './assets/data/articles.json'
</script>

<template>
  <Header />
  <main class="container">
    <FrontPage :data="data.frontPage" />
    <ArticleCard :data="data.articlesList" />
  </main>
  <Footer />
</template>

<style scoped></style>
