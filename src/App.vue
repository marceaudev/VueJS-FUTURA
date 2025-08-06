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
    <section>
      <ArticleCard v-for="article in data.articlesList" :key="article.id" :article="article" />
    </section>
  </main>
  <Footer />
</template>

<style scoped>
section {
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
  margin-top: 70px;
}
</style>
