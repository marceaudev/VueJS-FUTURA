<template>
  <footer>
    <p>
      Réalisé par
      <span><a href="https://github.com/marceaudev" target="_blank">Marceau</a></span> avec
      <span>VueJS</span>
    </p>
  </footer>
</template>

<style scoped>
footer {
  margin-top: 50px;
  width: 100%;
  display: flex;
  height: 50px;
  align-items: center;
  justify-content: center;
  position: relative;
}

footer::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 2px;
  background: linear-gradient(0.25turn, var(--light-purple), var(--dark-purple));
  top: 0;
}

span {
  font-weight: bold;
  background: linear-gradient(0.25turn, var(--light-purple), var(--dark-purple));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
