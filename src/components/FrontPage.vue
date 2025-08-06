<script setup>
defineProps({
  data: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <section :style="{ backgroundImage: `url(${data.image})` }">
    <div>
      <div>
        <div>
          <p>{{ data.category.toUpperCase() }}</p>
          <p>{{ data.subCategory.toUpperCase() }}</p>
        </div>
        <h1>
          <span>{{ data.title }}</span>
        </h1>
      </div>
      <div>
        <p>{{ data.teaser }}</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  height: 550px;
  width: 100%;
  margin-top: 50px;
  position: relative;
  display: flex;
}

img {
  height: 100%;
  width: 100%;
  object-fit: cover;
  object-position: bottom;
}

section > div {
  position: absolute;
  top: 25%;
  padding: 0 75px;
  display: flex;
  flex-direction: column;
  gap: 50px;
}

section > div > div:first-child {
  display: flex;
  flex-direction: column;
  position: relative;
  padding: 0 3px;
}

section > div > div:first-child::before {
  content: '';
  position: absolute;
  width: 4px;
  height: 100%;
  background: linear-gradient(0.5turn, var(--light-purple), var(--dark-purple));
  left: 0;
}

section > div > div > div {
  display: flex;
  gap: 15px;
  color: white;
  background-color: black;
  width: fit-content;
  padding: 5px 3px;
  font-size: 13px;
}

section > div > div > div p:first-child {
  background: linear-gradient(0.25turn, var(--light-purple), var(--dark-purple));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

h1 {
  font-family: 'Merriweather', serif;
  font-size: 32px;
  line-height: 46px;
  color: white;
  width: 750px;
  font-weight: bold;
}

span {
  padding: 5px;
  background-color: black;
  white-space: pre-wrap;
}

section > div > div:last-child {
  width: 68%;
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  padding: 25px;
  line-height: 24px;
  font-weight: lighter;
}
</style>
