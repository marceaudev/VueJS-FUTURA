<script setup>
defineProps({
  data: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <section>
    <div v-for="article in data" :key="article.id">
      <img :src="article.image" alt="Image de l'article" />
      <div>
        <p>{{ article.category.toUpperCase() }}</p>
        <p>{{ article.subCategory.toUpperCase() }}</p>
      </div>
      <h2>{{ article.title }}</h2>
      <span>{{ article.date }}</span>
    </div>
  </section>
</template>

<style scoped>
section {
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
  margin-top: 70px;
}

section > div {
  height: 480px;
  width: calc((100% - 90px) / 4);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

section > div:hover {
  cursor: pointer;
  transform: scale(1.01);
}

section img {
  width: 100%;
  min-height: 75%;
  max-height: 75%;
  object-fit: cover;
}

section > div > div {
  display: flex;
  gap: 15px;
  font-size: 14px;
}

section > div > div p:first-child {
  font-weight: bold;
  background: linear-gradient(0.25turn, var(--light-purple), var(--dark-purple));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

h2 {
  font-family: 'Merriweather', serif;
  font-weight: bold;
  font-size: 15px;
}

span {
  font-size: 12px;
  color: rgb(189, 189, 189);
}
</style>
